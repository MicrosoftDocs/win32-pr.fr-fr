---
title: HelpContextID, propriété (objet Characters)
description: En savoir plus sur la propriété HelpContextID de l’objet Characters. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e751cb2d8834a6af2c3b816066d6051e3a28c767
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068185"
---
# <a name="helpcontextid-property-characters-object"></a><span data-ttu-id="8de43-104">HelpContextID, propriété (objet Characters)</span><span class="sxs-lookup"><span data-stu-id="8de43-104">HelpContextID Property (Characters Object)</span></span>

<span data-ttu-id="8de43-105">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8de43-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8de43-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="8de43-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8de43-107">Retourne ou définit un numéro de contexte associé pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="8de43-107">Returns or sets an associated context number for the character.</span></span> <span data-ttu-id="8de43-108">Utilisé pour fournir une aide contextuelle pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="8de43-108">Used to provide context-sensitive Help for the character.</span></span>

</dd> <dt>

<span data-ttu-id="8de43-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="8de43-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8de43-110">\*agents. \***caractères («**_CharacterID_\*_»)._ \*  \[  =  *Numéro* de la HelpContextID\]</span><span class="sxs-lookup"><span data-stu-id="8de43-110">*agent.\***Characters("**_CharacterID_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="8de43-111">Partie</span><span class="sxs-lookup"><span data-stu-id="8de43-111">Part</span></span>     | <span data-ttu-id="8de43-112">Description</span><span class="sxs-lookup"><span data-stu-id="8de43-112">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="8de43-113">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="8de43-113">*Number*</span></span> | <span data-ttu-id="8de43-114">Entier spécifiant un numéro de contexte valide.</span><span class="sxs-lookup"><span data-stu-id="8de43-114">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8de43-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="8de43-115">Remarks</span></span>

<span data-ttu-id="8de43-116">Pour prendre en charge l’aide contextuelle pour le caractère, assignez le numéro de contexte au caractère que vous utilisez pour la rubrique d’aide associée quand vous compilez votre fichier d’aide.</span><span class="sxs-lookup"><span data-stu-id="8de43-116">To support context-sensitive Help for the character, assign the context number to the character you use for the associated Help topic when you compile your Help file.</span></span> <span data-ttu-id="8de43-117">Cette propriété s’applique uniquement au client du caractère ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères du client.</span><span class="sxs-lookup"><span data-stu-id="8de43-117">This property applies only to the client of the character; the setting does not affect other clients of the character or other characters of the client.</span></span>

<span data-ttu-id="8de43-118">Si vous avez créé un fichier d’aide Windows pour votre application et défini la propriété [**HelpFile**](helpfile-property.md) du caractère, agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **true** et que l’utilisateur clique sur le caractère.</span><span class="sxs-lookup"><span data-stu-id="8de43-118">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character.</span></span> <span data-ttu-id="8de43-119">S’il existe un numéro de contexte dans le [**HelpContextID**](helpcontextid-property.md), l’agent appelle l’aide et recherche la rubrique identifiée par le numéro de contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="8de43-119">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="8de43-120">Le nombre de contextes actuels est la valeur de **HelpContextID** pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="8de43-120">The current context number is the value of **HelpContextID** for the character.</span></span>

> [!Note]  
> <span data-ttu-id="8de43-121">La génération d’un fichier d’aide requiert le compilateur d’aide Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8de43-121">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="8de43-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8de43-122">See Also</span></span>

[<span data-ttu-id="8de43-123">**HelpFile, propriété**</span><span class="sxs-lookup"><span data-stu-id="8de43-123">**HelpFile property**</span></span>](helpfile-property.md)


 

 




