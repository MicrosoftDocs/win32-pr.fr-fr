---
description: Sur les systèmes d’exploitation 64 bits, Windows Installer peut appeler des actions personnalisées qui ont été compilées pour des systèmes 32 bits ou 64 bits.
ms.assetid: fc370ab4-93f3-4e1e-9468-3454d4fee0be
title: Actions personnalisées 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fcd804152abd010f985aab3b92c0de73a2744f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756261"
---
# <a name="64-bit-custom-actions"></a><span data-ttu-id="593be-103">Actions personnalisées 64 bits</span><span class="sxs-lookup"><span data-stu-id="593be-103">64-Bit Custom Actions</span></span>

<span data-ttu-id="593be-104">Sur les systèmes d’exploitation 64 bits, Windows Installer peut appeler des actions personnalisées qui ont été compilées pour des systèmes 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="593be-104">On 64-bit operating systems, Windows Installer may call custom actions that have been compiled for 32-bit or 64-bit systems.</span></span>

<span data-ttu-id="593be-105">Une action personnalisée 64 bits basée sur des [scripts](scripts.md) doit être marquée explicitement comme une action personnalisée 64 bits en ajoutant le bit **msidbCustomActionType64BitScript** au type numérique actions personnalisées dans la colonne type de la [table CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="593be-105">A 64-bit custom action based on [Scripts](scripts.md) must be explicitly marked as a 64-bit custom action by adding the **msidbCustomActionType64BitScript** bit to the custom actions numeric type in the Type column of the [CustomAction table](customaction-table.md).</span></span>



| <span data-ttu-id="593be-106">Constante</span><span class="sxs-lookup"><span data-stu-id="593be-106">Constant</span></span>                             | <span data-ttu-id="593be-107">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="593be-107">Hexadecimal</span></span> | <span data-ttu-id="593be-108">Decimal</span><span class="sxs-lookup"><span data-stu-id="593be-108">Decimal</span></span> | <span data-ttu-id="593be-109">Signification</span><span class="sxs-lookup"><span data-stu-id="593be-109">Meaning</span></span>                                                           |
|--------------------------------------|-------------|---------|-------------------------------------------------------------------|
| <span data-ttu-id="593be-110">**msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="593be-110">**msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="593be-111">0x0001000</span><span class="sxs-lookup"><span data-stu-id="593be-111">0x0001000</span></span>   | <span data-ttu-id="593be-112">4096</span><span class="sxs-lookup"><span data-stu-id="593be-112">4096</span></span>    | <span data-ttu-id="593be-113">Il s’agit d’une action personnalisée 64 bits écrite dans des [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="593be-113">This is a 64-bit custom action written in [Scripts](scripts.md).</span></span> |



 

<span data-ttu-id="593be-114">Les actions personnalisées basées sur des [fichiers exécutables](executable-files.md) ou des [bibliothèques de liens dynamiques](dynamic-link-libraries.md) qui ont été respectées pour un système d’exploitation 64 bits ne nécessitent pas l’inclusion de ce bit supplémentaire dans la colonne type de la table CustomAction.</span><span class="sxs-lookup"><span data-stu-id="593be-114">Custom actions based on [Executable files](executable-files.md) or [Dynamic-Link Libraries](dynamic-link-libraries.md) that have been complied for a 64-bit operating systems do not require including this additional bit in the Type column of the CustomAction table.</span></span>

 

 



