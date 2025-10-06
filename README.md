export default function handler(req, res) {
  const { key } = req.query;

  if (key !== "Mushtaq1990") {
    return res.status(401).json({ error: "غلط API کلید۔ اجازت نہیں ہے۔" });
  }

  const knowledge = [
    {
      question: "دنیا کا سب سے پہلا انسان کون تھا؟",
      answer: "حضرت آدم علیہ السلام۔"
    },
    {
      question: "قرآن پاک کی پہلی وحی کہاں نازل ہوئی؟",
      answer: "غارِ حرا میں۔"
    },
    {
      question: "اسلام کا پہلا خلیفہ کون تھا؟",
      answer: "حضرت ابوبکر صدیق رضی اللہ عنہ۔"
    },
    {
      question: "قرآن میں کتنی سورتیں ہیں؟",
      answer: "قرآن مجید میں 114 سورتیں ہیں۔"
    },
    {
      question: "دنیا کا سب سے بڑا سمندر کون سا ہے؟",
      answer: "بحر الکاہل۔"
    }
  ];

  res.status(200).json({ knowledge });
}
