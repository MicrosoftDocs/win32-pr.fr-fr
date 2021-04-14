---
title: Autres moteurs de reconnaissance vocale compatibles avec Microsoft Agent
description: Autres moteurs de reconnaissance vocale compatibles avec Microsoft Agent
ms.assetid: fa87c592-c819-4dea-a1d0-6ccb25cc0bcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9855a0f5374d35634d02f808b46449a053cada9a
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104381599"
---
# <a name="other-speech-engines-compatible-with-microsoft-agent"></a><span data-ttu-id="a1fcb-103">Autres moteurs de reconnaissance vocale compatibles avec Microsoft Agent</span><span class="sxs-lookup"><span data-stu-id="a1fcb-103">Other Speech Engines Compatible with Microsoft Agent</span></span>

<span data-ttu-id="a1fcb-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a1fcb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="a1fcb-105">Outre les moteurs de reconnaissance vocale Microsoft fournis avec et prenant en charge Microsoft Agent, un certain nombre d’entreprises proposent également des moteurs de reconnaissance vocale avec prise en charge de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a1fcb-105">In addition to the Microsoft speech engines that are provided with and support Microsoft Agent, a number of companies also offer speech engines with support for Microsoft Agent.</span></span> <span data-ttu-id="a1fcb-106">Cette page vous donne une vue d’ensemble de ces moteurs qui peuvent être disponibles en anglais (États-Unis) et dans d’autres langues.</span><span class="sxs-lookup"><span data-stu-id="a1fcb-106">This page gives you a brief overview of such engines that may be available in U.S. English and other languages.</span></span> <span data-ttu-id="a1fcb-107">Vous trouverez des informations sur l’installation et l’accès, ainsi que la licence et la redistribution des moteurs sur leurs sites Web.</span><span class="sxs-lookup"><span data-stu-id="a1fcb-107">Information about how to install and access, as well as license and redistribute the engines can be found at their websites.</span></span>

<span data-ttu-id="a1fcb-108">Lorsque vous utilisez un moteur de reconnaissance vocale tiers, vous devez également installer Microsoft SAPI 4.0 en tant que fichiers binaires d’exécution afin que les moteurs soient correctement énumérés.</span><span class="sxs-lookup"><span data-stu-id="a1fcb-108">When using any third-party speech engine, you also need to install Microsoft SAPI 4.0a runtime binaries so that the engines are enumerated properly.</span></span> <span data-ttu-id="a1fcb-109">À partir de votre page Web, vous pouvez inclure la balise suivante pour déclencher un téléchargement à partir de l’API Speech :</span><span class="sxs-lookup"><span data-stu-id="a1fcb-109">From your webpage you can include the following tag to trigger an autodownload of the Speech API:</span></span>

``` syntax
<OBJECT WIDTH=0 HEIGHT=0
  CLASSID="CLSID:0C7F3F20-8BAB-11d2-9432-00C04F8EF48F"
  CODEBASE="#VERSION=4,0,0,0">
</OBJECT>
```

<span data-ttu-id="a1fcb-110">Pour plus d’informations sur les fichiers binaires du runtime SAPI, reportez-vous au [site Web du groupe Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="a1fcb-110">For more information about the SAPI runtime binaries, refer to the [Microsoft Speech group's website](https://msdn.microsoft.com/library/ee705648.aspx).</span></span> <span data-ttu-id="a1fcb-111">Microsoft Agent installe également les fichiers binaires du runtime SAPI avec le moteur de reconnaissance vocale Microsoft, le panneau de configuration vocal et l’éditeur de caractères de l’agent.</span><span class="sxs-lookup"><span data-stu-id="a1fcb-111">Microsoft Agent also installs the SAPI runtime binaries with the Microsoft Speech Recognition Engine, the Speech Control Panel, and the Agent Character Editor.</span></span>

<span data-ttu-id="a1fcb-112">Veuillez noter que ces liens pointent vers des serveurs qui ne sont pas sous Microsoft Control.</span><span class="sxs-lookup"><span data-stu-id="a1fcb-112">Please note that these links point to servers that are not under Microsoft control.</span></span> <span data-ttu-id="a1fcb-113">Veuillez lire la [déclaration officielle](https://www.microsoft.com/isapi/gomscom.asp?TARGET=/Misc/NonMS.md) Microsoft concernant les autres serveurs.</span><span class="sxs-lookup"><span data-stu-id="a1fcb-113">Please read the Microsoft [official statement](https://www.microsoft.com/isapi/gomscom.asp?TARGET=/Misc/NonMS.md) regarding other servers.</span></span> <span data-ttu-id="a1fcb-114">Microsoft n’approuve pas le contenu ni les logiciels fournis sur ces sites Web.</span><span class="sxs-lookup"><span data-stu-id="a1fcb-114">Microsoft does not endorse the content nor the software provided at these websites.</span></span> <span data-ttu-id="a1fcb-115">Toutes les questions techniques et de support doivent également être adressées aux fournisseurs des moteurs et non à Microsoft ou à l’équipe Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a1fcb-115">All technical and support questions should also be directed to the suppliers of the engines and not to Microsoft or the Microsoft Agent team.</span></span>

<span data-ttu-id="a1fcb-116">**Digalo moteur de synthèse vocale**</span><span class="sxs-lookup"><span data-stu-id="a1fcb-116">**Digalo Text-To-Speech Engine**</span></span>

<span data-ttu-id="a1fcb-117">Digalo est un moteur TTS abordable conçu pour les utilisateurs finaux et les développeurs.</span><span class="sxs-lookup"><span data-stu-id="a1fcb-117">Digalo is an affordable TTS engine designed for end-users and developers.</span></span> <span data-ttu-id="a1fcb-118">Le moteur est proposé dans un certain nombre de langages : français, allemand, portugais (Brésil), espagnol, russe et anglais des États-Unis, avec l’italien, le polonais et d’autres langues disponibles prochainement.</span><span class="sxs-lookup"><span data-stu-id="a1fcb-118">The engine is offered in a number of languages: French, German, Portuguese (Brazil), Spanish, Russian, and UK and U.S. English, with Italian, Polish, and other languages coming soon.</span></span> <span data-ttu-id="a1fcb-119">Des informations sur les développeurs, ainsi que des détails sur l’inscription des utilisateurs finaux et les programmes d’affiliation, sont également disponibles.</span><span class="sxs-lookup"><span data-stu-id="a1fcb-119">Developer information, as well as details on end-user registration and affiliate programs, is also available.</span></span>

<span data-ttu-id="a1fcb-120">**Moteur de reconnaissance réseau ELAN**</span><span class="sxs-lookup"><span data-stu-id="a1fcb-120">**Elan Speech Engine**</span></span>

<span data-ttu-id="a1fcb-121">Le moteur de reconnaissance vocale Elan utilise la technologie de conversion de texte par synthèse vocale du réseau ELAN et est disponible en sept langues : français, allemand, portugais (Brésil), espagnol, russe, Royaume-Uni et anglais des États-Unis.</span><span class="sxs-lookup"><span data-stu-id="a1fcb-121">Elan Speech Engine uses Elan's Text To Speech technology and is available in seven languages: French, German, Portuguese (Brazil), Spanish, Russian, UK and U.S. English.</span></span>

<span data-ttu-id="a1fcb-122">**IBM ViaVoice-haute**</span><span class="sxs-lookup"><span data-stu-id="a1fcb-122">**IBM ViaVoice Outloud**</span></span>

<span data-ttu-id="a1fcb-123">IBM a développé plusieurs caractères Microsoft Agent pour une utilisation avec ViaVoice-bruyant.</span><span class="sxs-lookup"><span data-stu-id="a1fcb-123">IBM has developed several Microsoft Agent characters for use with ViaVoice Outloud.</span></span> <span data-ttu-id="a1fcb-124">IBM ViaVoice-bruyant est une technologie de synthèse vocale et est disponible en français, allemand, italien, espagnol, anglais du Royaume-Uni et anglais des États-Unis.</span><span class="sxs-lookup"><span data-stu-id="a1fcb-124">IBM ViaVoice Outloud is a text-to-speech (speech synthesis) technology and is available in French, German, Italian, Spanish, UK English and U.S. English.</span></span> <span data-ttu-id="a1fcb-125">Lorsqu’il est associé à Microsoft Agent, vous pouvez créer des applications vivantes dans de nombreuses langues et étendre vos opportunités commerciales à de nouveaux marchés internationaux.</span><span class="sxs-lookup"><span data-stu-id="a1fcb-125">When combined with Microsoft Agent, you can create vibrant applications in many languages and extend your sales opportunities to new worldwide markets.</span></span>

 

 




