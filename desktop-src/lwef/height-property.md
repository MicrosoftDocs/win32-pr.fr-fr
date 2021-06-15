---
title: Propriété Height (objet Characters)
description: En savoir plus sur la propriété Height de l’objet Characters. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93d288276bd9717378c9a1ab0d9b00489959c00
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068509"
---
# <a name="height-property-characters-object"></a><span data-ttu-id="a3839-104">Propriété Height (objet Characters)</span><span class="sxs-lookup"><span data-stu-id="a3839-104">Height Property (Characters Object)</span></span>

<span data-ttu-id="a3839-105">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a3839-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a3839-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="a3839-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a3839-107">Retourne ou définit la hauteur du cadre du caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="a3839-107">Returns or sets the height of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="a3839-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="a3839-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a3839-109">\*agent \***. Caractères («**_CharacterID_\*_»)._ \*  \[ =  *Valeur* de hauteur\]</span><span class="sxs-lookup"><span data-stu-id="a3839-109">*agent\***.Characters ("**_CharacterID_*_").Height_\* \[= *value*\]</span></span>



| <span data-ttu-id="a3839-110">Partie</span><span class="sxs-lookup"><span data-stu-id="a3839-110">Part</span></span>    | <span data-ttu-id="a3839-111">Description</span><span class="sxs-lookup"><span data-stu-id="a3839-111">Description</span></span>                                                 |
|---------|-------------------------------------------------------------|
| <span data-ttu-id="a3839-112">*value*</span><span class="sxs-lookup"><span data-stu-id="a3839-112">*value*</span></span> | <span data-ttu-id="a3839-113">Entier long qui spécifie la hauteur du frame du caractère.</span><span class="sxs-lookup"><span data-stu-id="a3839-113">A Long integer that specifies the character's frame height.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3839-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a3839-114">Remarks</span></span>

<span data-ttu-id="a3839-115">La propriété **Height** est toujours exprimée en pixels, par rapport aux coordonnées d’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="a3839-115">The **Height** property is always expressed in pixels, relative to screen coordinates (upper left).</span></span> <span data-ttu-id="a3839-116">Le paramètre de cette propriété s’applique à tous les clients du caractère.</span><span class="sxs-lookup"><span data-stu-id="a3839-116">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="a3839-117">Même si le caractère apparaît dans une fenêtre de zone de forme irrégulière, la hauteur du caractère est basée sur les dimensions externes du cadre d’animation rectangulaire utilisé lorsque le caractère a été compilé avec l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a3839-117">Even though the character appears in an irregularly shaped region window, the height of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




