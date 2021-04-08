---
title: HelpContextID, propriété (objet Command)
description: HelpContextID, propriété
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ef0fcfb24aee7aed75f8eb794e81291207ea24
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102753"
---
# <a name="helpcontextid-property-command-object"></a><span data-ttu-id="e4c73-103">HelpContextID, propriété (objet Command)</span><span class="sxs-lookup"><span data-stu-id="e4c73-103">HelpContextID Property (Command Object)</span></span>

<span data-ttu-id="e4c73-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e4c73-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e4c73-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="e4c73-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e4c73-106">Retourne ou définit un numéro de contexte associé pour l’objet de [**commande**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="e4c73-106">Returns or sets an associated context number for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="e4c73-107">Utilisé pour fournir une aide contextuelle pour l’objet de **commande** .</span><span class="sxs-lookup"><span data-stu-id="e4c73-107">Used to provide context-sensitive Help for the **Command** object.</span></span>

</dd> <dt>

<span data-ttu-id="e4c73-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="e4c73-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e4c73-109">\*agents. \***caractères («**_CharacterID_\*_»). Commandes («»)._ \*  \[  =  *Numéro* de la HelpContextID\]</span><span class="sxs-lookup"><span data-stu-id="e4c73-109">*agent.\***Characters("**_CharacterID_*_").Commands("").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="e4c73-110">Partie</span><span class="sxs-lookup"><span data-stu-id="e4c73-110">Part</span></span>     | <span data-ttu-id="e4c73-111">Description</span><span class="sxs-lookup"><span data-stu-id="e4c73-111">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="e4c73-112">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="e4c73-112">*Number*</span></span> | <span data-ttu-id="e4c73-113">Entier spécifiant un numéro de contexte valide.</span><span class="sxs-lookup"><span data-stu-id="e4c73-113">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4c73-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e4c73-114">Remarks</span></span>

<span data-ttu-id="e4c73-115">Si vous avez créé un fichier d’aide Windows pour votre application et défini la propriété [**HelpFile**](helpfile-property.md) du caractère sur le fichier, agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **true** et que l’utilisateur sélectionne la commande.</span><span class="sxs-lookup"><span data-stu-id="e4c73-115">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property to the file, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="e4c73-116">Si vous définissez un numéro de contexte dans le [**HelpContextID**](helpcontextid-property.md), l’agent appelle l’aide et recherche la rubrique identifiée par le numéro de contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="e4c73-116">If you set a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="e4c73-117">Le nombre de contextes actuels est la valeur de **HelpContextID** pour la commande.</span><span class="sxs-lookup"><span data-stu-id="e4c73-117">The current context number is the value of **HelpContextID** for the command.</span></span>

<span data-ttu-id="e4c73-118">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="e4c73-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="e4c73-119">La génération d’un fichier d’aide requiert le compilateur d’aide Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e4c73-119">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="e4c73-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4c73-120">See Also</span></span>

[<span data-ttu-id="e4c73-121">**HelpFile, propriété**</span><span class="sxs-lookup"><span data-stu-id="e4c73-121">**HelpFile property**</span></span>](helpfile-property.md)


 

 
