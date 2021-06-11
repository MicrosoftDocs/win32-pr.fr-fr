---
title: Propriété Left (objet Characters)
description: En savoir plus sur la propriété de l’objet Characters de gauche. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e2f860e6827a9c96c42014456e43b791ab70ed4
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988935"
---
# <a name="left-property-characters-object"></a><span data-ttu-id="0ef0b-104">Propriété Left (objet Characters)</span><span class="sxs-lookup"><span data-stu-id="0ef0b-104">Left Property (Characters Object)</span></span>

<span data-ttu-id="0ef0b-105">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0ef0b-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0ef0b-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="0ef0b-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0ef0b-107">Retourne ou définit le bord gauche du cadre du caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="0ef0b-107">Returns or sets the left edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="0ef0b-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="0ef0b-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0ef0b-109">\*agent \***. Caractères («**_CharacterID_\*_»)._ \*  \[  =  *Valeur* de gauche\]</span><span class="sxs-lookup"><span data-stu-id="0ef0b-109">*agent\***.Characters ("**_CharacterID_*_").Left_\* \[ = *value*\]</span></span>



| <span data-ttu-id="0ef0b-110">Partie</span><span class="sxs-lookup"><span data-stu-id="0ef0b-110">Part</span></span>    | <span data-ttu-id="0ef0b-111">Description</span><span class="sxs-lookup"><span data-stu-id="0ef0b-111">Description</span></span>                                                           |
|---------|-----------------------------------------------------------------------|
| <span data-ttu-id="0ef0b-112">*value*</span><span class="sxs-lookup"><span data-stu-id="0ef0b-112">*value*</span></span> | <span data-ttu-id="0ef0b-113">Entier long qui spécifie le bord gauche du frame du caractère.</span><span class="sxs-lookup"><span data-stu-id="0ef0b-113">A Long integer that specifies the left edge of the character's frame.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ef0b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0ef0b-114">Remarks</span></span>

<span data-ttu-id="0ef0b-115">La propriété **Left** est toujours exprimée en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="0ef0b-115">The **Left** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="0ef0b-116">Le paramètre de cette propriété s’applique à tous les clients du caractère.</span><span class="sxs-lookup"><span data-stu-id="0ef0b-116">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="0ef0b-117">Même si le caractère apparaît dans une fenêtre de zone de forme irrégulière, l’emplacement du caractère est basé sur les dimensions externes du cadre d’animation rectangulaire utilisé lorsque le caractère a été compilé avec l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="0ef0b-117">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




