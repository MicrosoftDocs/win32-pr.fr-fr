---
title: Propriété Left (objet Characters)
description: Propriété Left
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a318e659405883c56f296a9371eba7e9423662b1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106509497"
---
# <a name="left-property-characters-object"></a><span data-ttu-id="ed736-103">Propriété Left (objet Characters)</span><span class="sxs-lookup"><span data-stu-id="ed736-103">Left Property (Characters Object)</span></span>

<span data-ttu-id="ed736-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ed736-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ed736-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="ed736-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ed736-106">Retourne ou définit le bord gauche du cadre du caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="ed736-106">Returns or sets the left edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="ed736-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="ed736-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ed736-108">\*agent \***. Caractères («**_CharacterID_\*_»)._ \*  \[  =  *Valeur* de gauche\]</span><span class="sxs-lookup"><span data-stu-id="ed736-108">*agent\***.Characters ("**_CharacterID_*_").Left_\* \[ = *value*\]</span></span>



| <span data-ttu-id="ed736-109">Partie</span><span class="sxs-lookup"><span data-stu-id="ed736-109">Part</span></span>    | <span data-ttu-id="ed736-110">Description</span><span class="sxs-lookup"><span data-stu-id="ed736-110">Description</span></span>                                                           |
|---------|-----------------------------------------------------------------------|
| <span data-ttu-id="ed736-111">*value*</span><span class="sxs-lookup"><span data-stu-id="ed736-111">*value*</span></span> | <span data-ttu-id="ed736-112">Entier long qui spécifie le bord gauche du frame du caractère.</span><span class="sxs-lookup"><span data-stu-id="ed736-112">A Long integer that specifies the left edge of the character's frame.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed736-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ed736-113">Remarks</span></span>

<span data-ttu-id="ed736-114">La propriété **Left** est toujours exprimée en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="ed736-114">The **Left** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="ed736-115">Le paramètre de cette propriété s’applique à tous les clients du caractère.</span><span class="sxs-lookup"><span data-stu-id="ed736-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="ed736-116">Même si le caractère apparaît dans une fenêtre de zone de forme irrégulière, l’emplacement du caractère est basé sur les dimensions externes du cadre d’animation rectangulaire utilisé lorsque le caractère a été compilé avec l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="ed736-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




