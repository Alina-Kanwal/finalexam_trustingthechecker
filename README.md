Bar = kam se kam itna jitna hona chahiye, tab hi kaam ko "theek" maana jayega. Jaise imtihan mein pass marks.
Tuning = rule, prompt ya hidayat ko baar baar badal kar score behtar karna. Jaise cases fail hon to rule thoda badla, dobara chalaya, phir badla.
Origin = case ki file mein ek line jo batati hai ke yeh ghalti kahan se aayi.(human deta hy)
PASS ka matlab: is ek kaam ko checker ne theek kaha.
Kai baar chalana isliye: ta ke pata chale ke agent aam taur par kitni baar theek karta hai, sirf is ek baar nahi.
Rubric = judge ki marking guide: har number ka matlab, ek asal misaal ke saath. Rubric judge ke liye hoti hai, aur usay insaan (aap ya team) likhta hai, judge nahi. Judge ko usi rubric ke hisaab se parakhna hota hai, aur baad mein aap judge ko parakhte hain ke woh rubric par kitna chalta hai.
Jawab: agent ne kya likha. Ghalat jawab aur toota hua format yahan pakde jate hain, lekin "jawab theek lagta hai magar kaam ghalat hua" yahan nahi pakda jata.
Kaam: agent ne asal mein kya kiya. Aap ki transactions yahan aati hain. Coding mein iski jagah diff aur log hote hain.
Raasta: poora safar, yani kadam, dobara koshishein aur unka order. Yahan woh kharabi pakdi jati hai jo is baar chal gayi lekin agli baar nahi chalegi.
Test: ek cheez ko ek baar dekhta hai. 2 + 2 = 4 jaisi cheez, jahan jawab kabhi nahi badalta.
Eval: wahi kaam kai baar chalata hai aur ginta hai kitni baar theek hua. Bus(Roz ati hy or alg time pr) jaisi cheez ke liye, jahan natija badalta rehta hai.
Ek PASS kaafi nahi: agent ka jawab kabhi alag aa sakta hai, isliye ek PASS sirf itna batata hai ke is baar PASS aaya.
Natija ek andaza hota hai: "20 mein se 17" ka matlab hai ke abhi takreeban itna theek hai. Yeh pakka waada nahi.
Bar ghalti ki keemat se tay hota hai: refund jaise kaam par 20/20 chahiye, salaam jaise chhote kaam par kam chal sakta hai.
checker khud bhi ghalat ho sakta hai, aur agar usay koi nahi parakhta to uska ghalat PASS bhi sach jaisa lagta hai. Isi liye use bhi jaanchte hain.
glti ko save rakhein ek folder mein, har case ek chhoti alag file. Jaise evals/cases/ folder, aur us mein deleted-test-001.json. Is folder ko wahin rakhein jahan aap ka code hai, taake har badlaav ke saath uski history bhi rahe.
Judge wahi checker hai jo PASS ya FAIL deta hai,
Rubric (judge ke liye, 3 cheezein):
Kya dekhna hai: judge ko haan/nahi wale saaf sawal, jaise "kya koi test delete hua?"
Har nateeje ka matlab: kab 5, kab 3, kab PASS, kab FAIL.
Asal misalein: har nateeje ke saath ek purana asal kaam, taake naye kaam se mila saken.
Case (ek ghalti ka record, 4 cheezein):
Input: woh kaam ya diff jo judge ko parakhna hai.
Expected: sahi nateeja kya hona chahiye tha, jaise FAIL.
Unacceptable: jo cheez kabhi nazar nahi aani chahiye, jaise "test hata hua aur phir bhi PASS".
Origin: yeh ghalti kahan se aayi, jaise ticket number.
/////////////////////////////////////////////OVERALL Y HAY KEA??
Maan lein aap ki team mein ek naya saathi (agent) aaya hai jo customers ko jawab deta hai, aur ek supervisor (judge) hai jo uske jawab parakhti hai. Ab sawal yeh hai: supervisor ki marking par kaise bharosa karein?
Ek baar ka PASS kaafi nahi. Saathi ek din theek kaam kare to kal bhi theek karega, yeh pakka nahi. Isliye kaam kai baar dekhte hain.
Register banate hain. Jab bhi saathi ki koi asal ghalti pakdi jaye, uska ek safha (case) register mein likh lete hain.
Supervisor ko marking sheet dete hain (rubric). Taake woh apne mood se number na de.
Supervisor ko bhi parakhte hain. Aap 20 jawab khud check karti hain aur dekhti hain ke aap dono ka fe'sla kitna milta hai. Sab se bura farq wahi hai jahan supervisor ne ghalat kaam ko PASS kar diya.
Jab bhi kuch badle, register dobara chalate hain. Naya rule aaye to dekhte hain ke purani ghalti wapas to nahi aayi.
Waqt waqt par register chalate rehte hain. Kyunki kabhi kabhi aap kuch nahi badalti, phir bhi saathi ka behaviour badal jata hai. 
1. Har baar PASS zaroori nahi hota. Yeh bar par depend karta hai. Refund jaise mehngi ghalti par har baar PASS chahiye (6 mein se 6). Lehje jaise sasti ghalti par 80% bhi chalta hai. Hum PASS isliye dekhte hain ke pata chale agent par kitna bharosa kar saken, isliye nahi ke har baar 100% laazmi ho.
2. Haan, insaan checker ko bhi verify karta hai, lekin har baar nahi. Insaan ek chhoti jaanch karta hai: 20 fe'sle uthata hai, khud rubric ke mutabik check karta hai, aur dekhta hai ke checker se kitna milta hai. Yeh kabhi kabhi hota hai, har PASS par nahi. Aur khatarnak kaam (jaise paisa) aakhir mein phir bhi insaan ke paas jata hai.
Jis my mistakes likhi hoti hain taaaky wo dubara na hon wo yahan wo har baar poora folder chalana mehnga padta hai, kyunki har run model ke paise lagata hai. Isliye suite ko teen hisson mein baant dete hain:
Chhota set (smoke set): sab se zaroori 5-6 cases, har badlaav par chalte hain, kuch minute mein.
Poora set: saare cases, raat ko schedule par.
Hold-outs: kuch cases jin par aap ne kabhi tuning (changes jo tha wohi raha) nahi ki, hafte mein ek baar computer chalayega. Laken agr tuned case m changes hojaye tw wo tuned ni rehta blky pora set my chala jata hy.
Chhota tareeqa jaldi aur sasta hai, isliye har badlaav/changes
Bada tareeqa dair aur paisa leta hai, isliye wahi raat ko ya hafte mein ek baar. 
Case green tab rehta hai jab agent us case mein sahi kaam kar raha ho, yani purani ghalti dobara nahi ho rahi. Jaise hi ghalti wapas aaye, case red ho jata hai.
2. Chhota set, poora set, hold-outs.
Chhota set poore set ka hissa hai. Poore set ke saare cases mein se sab se zaroori 5-6 cases chhote set mein bhi rakhte hain.
Hold-outs poore set ka hissa nahi hain. Wo alag, seal kiye hue cases hain jin par tuning nahi hui.
Alina: insaan ko bhi purane sawal aasaan lagte hain, naye mushkil. AI ke saath bhi yahi hota hai. Fark yeh hai ke aap ko apna ratta mehsoos hota hai, jabke computer ka ratta aap ko score dekh kar hi pata chalta hai. Isliye hold-outs rakhte hain: naya imtihan, taake pata chale ke asal samajh hai ya sirf ratta.
Ek lafz ki wazahat: in sets mein rules nahi hote, cases hote hain. Rule wo hai jo aap agent ko dete hain (prompt ya hidayat). Aur har case ke saath ek bar hota hai: kitne PASS par case theek maana jaye.
Jab hold-out par ghalti pakad kar rule badlein, to wo case ab hold-out nahi raha, wo poore set mein chala jata hai.
Reviewer/judge/checker ak hi hai,
Verdict = judge ka faisla ek kaam par: PASS ya FAIL (saath mein reasons aur risk). Jaise ek exam ka result: pass ya fail.
Misaal: judge ne ek diff dekha aur likha {"verdict": "FAIL", "reasons": ["test deleted"], "risk": "high"}. Yeh ek verdict hai.



































