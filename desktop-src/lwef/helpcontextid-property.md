---
title: HelpContextID, propriété (objet collection Commands)
description: HelpContextID, propriété
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d530a1563080108ef2a2798589519ecca03416
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464111"
---
# <a name="helpcontextid-property-commands-collection-object"></a><span data-ttu-id="0c4fd-103">HelpContextID, propriété (objet collection Commands)</span><span class="sxs-lookup"><span data-stu-id="0c4fd-103">HelpContextID Property (Commands Collection Object)</span></span>

<span data-ttu-id="0c4fd-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0c4fd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0c4fd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="0c4fd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0c4fd-106">Retourne ou définit un numéro de contexte associé pour l’objet [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="0c4fd-106">Returns or sets an associated context number for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="0c4fd-107">Utilisé pour fournir une aide contextuelle pour l’objet **Commands** .</span><span class="sxs-lookup"><span data-stu-id="0c4fd-107">Used to provide context-sensitive Help for the **Commands** object.</span></span>

</dd> <dt>

<span data-ttu-id="0c4fd-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="0c4fd-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0c4fd-109">\*agents. \***caractères («**_CharacterID_*_»). Commandes («_*_nom_\*_»)._ \*  \[  =  *Numéro* de la HelpContextID\]</span><span class="sxs-lookup"><span data-stu-id="0c4fd-109">*agent.\***Characters("**_CharacterID_*_").Commands("_*_name_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="0c4fd-110">Partie</span><span class="sxs-lookup"><span data-stu-id="0c4fd-110">Part</span></span>     | <span data-ttu-id="0c4fd-111">Description</span><span class="sxs-lookup"><span data-stu-id="0c4fd-111">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="0c4fd-112">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="0c4fd-112">*Number*</span></span> | <span data-ttu-id="0c4fd-113">Entier spécifiant un numéro de contexte valide.</span><span class="sxs-lookup"><span data-stu-id="0c4fd-113">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c4fd-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0c4fd-114">Remarks</span></span>

<span data-ttu-id="0c4fd-115">Si vous avez créé un fichier d’aide Windows pour votre application et défini la propriété [**HelpFile**](helpfile-property.md) du caractère, agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **true** et que l’utilisateur sélectionne l’objet [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="0c4fd-115">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="0c4fd-116">Si vous définissez un numéro de contexte dans la **HelpContextID**, l’agent appelle l’aide et recherche la rubrique identifiée par ce numéro de contexte.</span><span class="sxs-lookup"><span data-stu-id="0c4fd-116">If you set a context number in the **HelpContextID**, Agent calls Help and searches for the topic identified by that context number.</span></span>

<span data-ttu-id="0c4fd-117">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="0c4fd-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="0c4fd-118">La génération d’un fichier d’aide requiert le compilateur d’aide Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0c4fd-118">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="0c4fd-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c4fd-119">See Also</span></span>

[<span data-ttu-id="0c4fd-120">**HelpFile, propriété**</span><span class="sxs-lookup"><span data-stu-id="0c4fd-120">**HelpFile property**</span></span>](helpfile-property.md)


 

 
