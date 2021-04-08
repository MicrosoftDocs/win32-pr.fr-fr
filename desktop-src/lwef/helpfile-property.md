---
title: HelpFile, propriété
description: HelpFile, propriété
ms.assetid: 18a5fd9b-4ca7-4701-9993-1e0c55f6e232
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d5307abfba0f884261f5b4a21131a75cf87224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673481"
---
# <a name="helpfile-property"></a><span data-ttu-id="b516b-103">HelpFile, propriété</span><span class="sxs-lookup"><span data-stu-id="b516b-103">HelpFile Property</span></span>

<span data-ttu-id="b516b-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b516b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b516b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="b516b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b516b-106">Retourne ou définit le chemin d’accès et le nom de fichier d’un fichier d’aide contextuelle Microsoft Windows fourni par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="b516b-106">Returns or sets the path and filename for a Microsoft Windows context-sensitive Help file supplied by the client application.</span></span>

</dd> <dt>

<span data-ttu-id="b516b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="b516b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b516b-108">\*agent. ***Caractères («*** CharacterID \* \* * »).* \*  \[  =  *Nom de fichier* HelpFile\]</span><span class="sxs-lookup"><span data-stu-id="b516b-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Helpfile** \[ = *Filename*\]</span></span>



| <span data-ttu-id="b516b-109">Partie</span><span class="sxs-lookup"><span data-stu-id="b516b-109">Part</span></span>       | <span data-ttu-id="b516b-110">Description</span><span class="sxs-lookup"><span data-stu-id="b516b-110">Description</span></span>                                                                    |
|------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="b516b-111">*Nom du fichier*</span><span class="sxs-lookup"><span data-stu-id="b516b-111">*Filename*</span></span> | <span data-ttu-id="b516b-112">Expression de chaîne spécifiant le chemin d’accès et le nom de fichier du fichier d’aide Windows.</span><span class="sxs-lookup"><span data-stu-id="b516b-112">A string expression specifying the path and filename of the Windows Help file.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b516b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b516b-113">Remarks</span></span>

<span data-ttu-id="b516b-114">Si vous avez créé un fichier d’aide Windows pour votre application et défini la propriété **HelpFile** du caractère, agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **true** et que l’utilisateur clique sur le caractère ou sélectionne une commande dans son menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="b516b-114">If you've created a Windows Help file for your application and set the character's **HelpFile** property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character or selects a command from its pop-up menu.</span></span> <span data-ttu-id="b516b-115">Si vous avez spécifié un numéro de contexte dans la propriété [**HelpContextID**](helpcontextid-property.md) de la commande sélectionnée, help affiche une rubrique correspondant au contexte d’aide actuel. Sinon, elle affiche « aucune rubrique d’aide associée à cet élément ».</span><span class="sxs-lookup"><span data-stu-id="b516b-115">If you specified a context number in the [**HelpContextID**](helpcontextid-property.md) property of the selected command, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="b516b-116">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="b516b-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="b516b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b516b-117">See Also</span></span>

<span data-ttu-id="b516b-118">[**Propriété HelpModeOn**](helpmodeon-property.md), [ **HelpContextID, propriété**](helpcontextid-property.md)</span><span class="sxs-lookup"><span data-stu-id="b516b-118">[**HelpModeOn property**](helpmodeon-property.md), [**HelpContextID property**](helpcontextid-property.md)</span></span>


 

 




