# untuk kamu
wanita yang aku sayang

import { useState } from "react"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { motion } from "framer-motion";

export default function CatatanUntukKamu() { const [image, setImage] = useState(null);

const handleImageUpload = (e) => { const file = e.target.files[0]; if (file) { const reader = new FileReader(); reader.onloadend = () => { setImage(reader.result); }; reader.readAsDataURL(file); } };

return ( <div className="min-h-screen bg-gradient-to-br from-gray-900 to-black text-white flex items-center justify-center p-6"> <motion.div initial={{ opacity: 0, y: 30 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 0.8 }} className="w-full max-w-3xl" > <Card className="rounded-2xl shadow-2xl bg-gray-800"> <CardContent className="p-8 space-y-6"> <h1 className="text-3xl font-bold text-center"> catatan tentang kamu </h1>

{image && (
          <motion.img
            src={image}
            alt="foto"
            initial={{ opacity: 0 }}
            animate={{ opacity: 1 }}
            transition={{ duration: 0.6 }}
            className="w-full rounded-2xl shadow-lg object-cover max-h-96"
          />
        )}

        <div className="text-base leading-relaxed space-y-4 text-gray-200">
          <p>
            kamu itu perempuan yang baik. perhatianmu sederhana tapi terasa dalam.
            caramu peduli selalu bikin aku merasa nggak sendirian.
          </p>
          <p>
            kamu cantik bukan cuma dari wajah, tapi dari caramu tersenyum dan
            tertawa tanpa dibuat-buat. kamu lucu, menggemaskan, dan kadang
            menyebalkan dengan cara yang bikin aku tetap bertahan.
          </p>
          <p>
            tapi aku juga jujur, kadang kata-katamu bikin aku jatuh. bukan
            karena aku benci kamu, tapi karena aku terlalu peduli.
        
