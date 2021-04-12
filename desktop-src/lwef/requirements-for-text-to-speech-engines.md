---
title: Configuration requise pour les moteurs de conversion de texte par synthèse vocale
description: Configuration requise pour les moteurs de conversion de texte par synthèse vocale
ms.assetid: 21d19949-c9b4-4d9c-9684-6d15162f7a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6d1bc9f4340327c5fbfb71b900e10f60738fdf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462258"
---
# <a name="requirements-for-text-to-speech-engines"></a><span data-ttu-id="24ac1-103">Configuration requise pour les moteurs de conversion de texte par synthèse vocale</span><span class="sxs-lookup"><span data-stu-id="24ac1-103">Requirements for Text-To-Speech Engines</span></span>

<span data-ttu-id="24ac1-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="24ac1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="24ac1-105">Le moteur doit être entièrement conforme à SAPI 4,0.</span><span class="sxs-lookup"><span data-stu-id="24ac1-105">The engine must be fully SAPI 4.0-compliant.</span></span> <span data-ttu-id="24ac1-106">En outre, le moteur doit également prendre en charge les interfaces SAPI suivantes pour les notifications de signets et de texte avec balises.</span><span class="sxs-lookup"><span data-stu-id="24ac1-106">In addition, the engine must also support the following SAPI interfaces for tagged text and bookmark notifications.</span></span> <span data-ttu-id="24ac1-107">Ces interfaces permettent à Microsoft Agent d’adapter la sortie du texte à la bulle d’un caractère et au lèvre de synchroniser la bouche du personnage (ou l’équivalent) avec les mots prononcés.</span><span class="sxs-lookup"><span data-stu-id="24ac1-107">These interfaces enable Microsoft Agent to pace the output of text to a character's word balloon and lip-sync the character's mouth (or equivalent) with the spoken words.</span></span>

-   [<span data-ttu-id="24ac1-108">ITTSCentralW</span><span class="sxs-lookup"><span data-stu-id="24ac1-108">ITTSCentralW</span></span>](ittscentralw.md)
-   [<span data-ttu-id="24ac1-109">ITTSNotifySinkW</span><span class="sxs-lookup"><span data-stu-id="24ac1-109">ITTSNotifySinkW</span></span>](ittsnotifysinkw.md)
-   [<span data-ttu-id="24ac1-110">ITTSBufNotifySinkW</span><span class="sxs-lookup"><span data-stu-id="24ac1-110">ITTSBufNotifySinkW</span></span>](ittsbufnotifysinkw.md)
-   [<span data-ttu-id="24ac1-111">ITTSAttributesW</span><span class="sxs-lookup"><span data-stu-id="24ac1-111">ITTSAttributesW</span></span>](ittsattributesw.md)

 

 




