---
title: Balises de sortie vocale Microsoft Agent
description: Balises de sortie vocale Microsoft Agent
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d365d4837df3e3a5afb57c355e229f21ade0b5a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840097"
---
# <a name="microsoft-agent-speech-output-tags"></a><span data-ttu-id="11efe-103">Balises de sortie vocale Microsoft Agent</span><span class="sxs-lookup"><span data-stu-id="11efe-103">Microsoft Agent Speech Output Tags</span></span>

<span data-ttu-id="11efe-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="11efe-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="11efe-105">Les services Microsoft Agent prennent en charge la modification de la sortie vocale par le biais de balises spéciales insérées dans la chaîne de texte vocal.</span><span class="sxs-lookup"><span data-stu-id="11efe-105">The Microsoft Agent services support modifying speech output through special tags inserted in the speech text string.</span></span> <span data-ttu-id="11efe-106">Ces balises vous aident à modifier les caractéristiques de l’expression de sortie du caractère.</span><span class="sxs-lookup"><span data-stu-id="11efe-106">These tags help you change the characteristics of the output expression of the character.</span></span>

<span data-ttu-id="11efe-107">Les balises de sortie vocale utilisent les règles de syntaxe suivantes :</span><span class="sxs-lookup"><span data-stu-id="11efe-107">Speech output tags use the following rules of syntax:</span></span>

-   <span data-ttu-id="11efe-108">Toutes les balises commencent et se terminent par une barre oblique inverse ( \) .</span><span class="sxs-lookup"><span data-stu-id="11efe-108">All tags begin and end with a backslash character (\).</span></span>
-   <span data-ttu-id="11efe-109">La barre oblique inverse unique n’est pas activée dans une balise.</span><span class="sxs-lookup"><span data-stu-id="11efe-109">The single backslash character is not enabled within a tag.</span></span> <span data-ttu-id="11efe-110">Pour inclure une barre oblique inverse dans un paramètre de texte d’une balise, utilisez une double barre oblique inverse ( \\ \) .</span><span class="sxs-lookup"><span data-stu-id="11efe-110">To include a backslash character in a text parameter of a tag, use a double backslash (\\\).</span></span>
-   <span data-ttu-id="11efe-111">Les balises ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="11efe-111">Tags are case-insensitive.</span></span> <span data-ttu-id="11efe-112">Par exemple, \\ Pit \\ est le même que \\ Pit \\ .</span><span class="sxs-lookup"><span data-stu-id="11efe-112">For example, \\pit\\ is the same as \\PIT\\.</span></span>
-   <span data-ttu-id="11efe-113">Les balises sont dépendantes des espaces blancs.</span><span class="sxs-lookup"><span data-stu-id="11efe-113">Tags are whitespace-dependent.</span></span> <span data-ttu-id="11efe-114">Par exemple, \\ RST \\ n’est pas le même \\ que \\ RST.</span><span class="sxs-lookup"><span data-stu-id="11efe-114">For example, \\Rst\\ is not the same as \\ Rst \\.</span></span>

<span data-ttu-id="11efe-115">Sauf indication contraire ou modification par une autre balise, la sortie vocale conserve la caractéristique définie par la balise dans le texte spécifié dans une méthode [**Speak**](speak-method.md) unique.</span><span class="sxs-lookup"><span data-stu-id="11efe-115">Unless otherwise specified or modified by another tag, the speech output retains the characteristic set by the tag within the text specified in a single [**Speak**](speak-method.md) method.</span></span> <span data-ttu-id="11efe-116">La sortie vocale est automatiquement réinitialisée via les paramètres définis par l’utilisateur après la fin d’une méthode **Speak** .</span><span class="sxs-lookup"><span data-stu-id="11efe-116">Speech output is automatically reset through the user-defined parameters after a **Speak** method is completed.</span></span>

<span data-ttu-id="11efe-117">Certaines balises incluent des chaînes entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="11efe-117">Some tags include quoted strings.</span></span> <span data-ttu-id="11efe-118">Pour certains langages de programmation, tels que Visual Basic Scripting Edition (VBScript) et Visual Basic, cela signifie que vous devrez peut-être utiliser deux guillemets pour désigner le paramètre de la balise ou concaténer un guillemet double comme faisant partie de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="11efe-118">For some programming languages, such as Visual Basic Scripting Edition (VBScript) and Visual Basic, this means that you may have to use two quote marks to designate the tag's parameter or concatenate a double-quote character as part of the string.</span></span> <span data-ttu-id="11efe-119">Ce dernier s’affiche dans cet exemple de Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="11efe-119">The latter is shown in this Visual Basic example:</span></span>


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



<span data-ttu-id="11efe-120">Pour la programmation en C, C++ et Java™, faites précéder les barres obliques inverses et les guillemets doubles d’une barre oblique inverse.</span><span class="sxs-lookup"><span data-stu-id="11efe-120">For C, C++, and Java™ programming, precede backslashes and double quotes with a backslash.</span></span> <span data-ttu-id="11efe-121">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="11efe-121">For example:</span></span>


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



<span data-ttu-id="11efe-122">Pour les langues étrangères qui prennent en charge les caractères DBCS (Double-Byte Character Set), vous pouvez utiliser des caractères codés sur deux octets pour spécifier des paramètres de chaîne.</span><span class="sxs-lookup"><span data-stu-id="11efe-122">For foreign languages that support double-byte character set (DBCS) characters, you can use double-byte characters to specify string parameters.</span></span> <span data-ttu-id="11efe-123">Toutefois, utilisez des caractères codés sur un octet pour tous les autres paramètres et caractères utilisés pour définir la balise, y compris l’étiquette elle-même.</span><span class="sxs-lookup"><span data-stu-id="11efe-123">However, use single-byte characters for all other parameters and characters that are used to define the tag, including the tag itself.</span></span>

<span data-ttu-id="11efe-124">Les balises suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="11efe-124">The following tags are supported:</span></span>

-   [<span data-ttu-id="11efe-125">**Chr**</span><span class="sxs-lookup"><span data-stu-id="11efe-125">**Chr**</span></span>](chr-tag.md)
-   [<span data-ttu-id="11efe-126">**CTX**</span><span class="sxs-lookup"><span data-stu-id="11efe-126">**Ctx**</span></span>](ctx-tag.md)
-   [<span data-ttu-id="11efe-127">**Renseignements**</span><span class="sxs-lookup"><span data-stu-id="11efe-127">**Emp**</span></span>](emp-tag.md)
-   [<span data-ttu-id="11efe-128">**LST**</span><span class="sxs-lookup"><span data-stu-id="11efe-128">**Lst**</span></span>](lst-tag.md)
-   [<span data-ttu-id="11efe-129">**Canal**</span><span class="sxs-lookup"><span data-stu-id="11efe-129">**Map**</span></span>](map-tag.md)
-   [<span data-ttu-id="11efe-130">**Mrk**</span><span class="sxs-lookup"><span data-stu-id="11efe-130">**Mrk**</span></span>](mrk-tag.md)
-   [<span data-ttu-id="11efe-131">**Pau**</span><span class="sxs-lookup"><span data-stu-id="11efe-131">**Pau**</span></span>](pau-tag.md)
-   [<span data-ttu-id="11efe-132">**Compose**</span><span class="sxs-lookup"><span data-stu-id="11efe-132">**Pit**</span></span>](pit-tag.md)
-   [<span data-ttu-id="11efe-133">**RST**</span><span class="sxs-lookup"><span data-stu-id="11efe-133">**Rst**</span></span>](rst-tag.md)
-   [<span data-ttu-id="11efe-134">**SPD**</span><span class="sxs-lookup"><span data-stu-id="11efe-134">**Spd**</span></span>](spd-tag.md)
-   [<span data-ttu-id="11efe-135">**Vol**</span><span class="sxs-lookup"><span data-stu-id="11efe-135">**Vol**</span></span>](vol-tag.md)

<span data-ttu-id="11efe-136">Les balises sont principalement conçues pour ajuster la sortie générée par la conversion de texte par synthèse vocale (TTS).</span><span class="sxs-lookup"><span data-stu-id="11efe-136">The tags are primarily designed for adjusting text-to-speech (TTS)-generated output.</span></span> <span data-ttu-id="11efe-137">Seules les balises [**MRK**](mrk-tag.md) et [**Map**](map-tag.md) peuvent être utilisées avec une sortie orale basée sur des fichiers audio.</span><span class="sxs-lookup"><span data-stu-id="11efe-137">Only the [**Mrk**](mrk-tag.md) and [**Map**](map-tag.md) tags can be used with sound file-based spoken output.</span></span>

> [!Note]  
> <span data-ttu-id="11efe-138">Microsoft Agent ne prend pas en charge toutes les balises documentées dans le kit de développement logiciel (SDK) Microsoft Speech.</span><span class="sxs-lookup"><span data-stu-id="11efe-138">Microsoft Agent does not support all the tags documented in the Microsoft Speech SDK.</span></span> <span data-ttu-id="11efe-139">Les paramètres peuvent également varier en fonction du moteur TTS sélectionné.</span><span class="sxs-lookup"><span data-stu-id="11efe-139">Parameters may also vary depending on the TTS engine selected.</span></span> <span data-ttu-id="11efe-140">Vous pouvez définir un moteur TTS spécifique à l’aide de [**TTSModeID**](ttsmodeid-property.md).</span><span class="sxs-lookup"><span data-stu-id="11efe-140">You can set a specific TTS engine using [**TTSModeID**](ttsmodeid-property.md).</span></span>

 

 

 




