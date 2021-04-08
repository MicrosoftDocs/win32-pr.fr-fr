---
description: Indique au compilateur MOF de séparer un fichier MOF en versions indépendantes du langage et spécifiques à la langue.
ms.assetid: c1aec33c-b936-4cca-8fcd-7bd088af7116
ms.tgt_platform: multiple
title: Amendement pragma
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1269ac1a96617b72852e687b2a38ce8d331ab3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753700"
---
# <a name="pragma-amendment"></a><span data-ttu-id="6378b-103">Amendement pragma</span><span class="sxs-lookup"><span data-stu-id="6378b-103">pragma amendment</span></span>

<span data-ttu-id="6378b-104">La commande de préprocesseur **pragma avenant** indique au compilateur MOF de séparer un fichier MOF en versions indépendantes du langage et spécifiques à la langue.</span><span class="sxs-lookup"><span data-stu-id="6378b-104">The **pragma amendment** preprocessor command directs the MOF compiler to separate a MOF file into language-neutral and language-specific versions.</span></span> <span data-ttu-id="6378b-105">Le fichier MOF propre au langage déplace les qualificateurs modifiés vers un espace de noms pour des paramètres régionaux spécifiques.</span><span class="sxs-lookup"><span data-stu-id="6378b-105">The language-specific MOF file moves amended qualifiers to a namespace for a specific locale.</span></span> <span data-ttu-id="6378b-106">Vous compilez ensuite les fichiers MOF propres au langage et à la langue pour stocker les informations de classe dans le référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="6378b-106">You then compile the language-specific and language-neutral MOF files to store class information in the WMI repository.</span></span>

## <a name="examples"></a><span data-ttu-id="6378b-107">Exemples</span><span class="sxs-lookup"><span data-stu-id="6378b-107">Examples</span></span>

<span data-ttu-id="6378b-108">L’exemple suivant montre comment créer un fichier MOF qui contient des qualificateurs modifiés.</span><span class="sxs-lookup"><span data-stu-id="6378b-108">The following example shows how to create a MOF file that contains amended qualifiers.</span></span> <span data-ttu-id="6378b-109">Vous pouvez ensuite compiler le code MOF avec la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="6378b-109">You can then compile the MOF code with the following command:</span></span>

<span data-ttu-id="6378b-110">**mofcomp** **-MOF : Lnmof. mof** **-MFL : Lsmof. MFL** **Mastermof. mof**</span><span class="sxs-lookup"><span data-stu-id="6378b-110">**mofcomp** **-MOF:Lnmof.mof** **-MFL:Lsmof.mfl** **Mastermof.mof**</span></span>

<span data-ttu-id="6378b-111">La commande indique au compilateur MOF de générer deux fichiers MOF à partir du fichier Mastermof. mof d’origine.</span><span class="sxs-lookup"><span data-stu-id="6378b-111">The command instructs the MOF compiler to produce two MOF files from the original Mastermof.mof file.</span></span> <span data-ttu-id="6378b-112">Le compilateur MOF produit une version indépendante du langage du fichier MOF, appelée Lnmof. mof, avec tous les éléments spécifiques à la langue supprimés.</span><span class="sxs-lookup"><span data-stu-id="6378b-112">The MOF compiler produces a language-neutral version of the MOF file, called Lnmof.mof, with all language-specific items removed.</span></span> <span data-ttu-id="6378b-113">Le compilateur crée également un second fichier MOF propre au langage appelé Lsmof. MFL qui contient uniquement les éléments que vous devez localiser.</span><span class="sxs-lookup"><span data-stu-id="6378b-113">The compiler also creates a second, language-specific MOF file called Lsmof.mfl that contains only items that you must localize.</span></span>

> [!Note]  
> <span data-ttu-id="6378b-114">Lorsque vous fractionnez un fichier MOF avec le qualificateur d' **Amendement** ou la commande **pragma avenant** , vous devez spécifier les options **-MOF** et **-MFL** .</span><span class="sxs-lookup"><span data-stu-id="6378b-114">When you are splitting a MOF file with the **amendment** qualifier or the **pragma amendment** command, you must specify the **-MOF** and **-MFL** options.</span></span> <span data-ttu-id="6378b-115">Sinon, le compilateur ne génère pas de fichiers de sortie.</span><span class="sxs-lookup"><span data-stu-id="6378b-115">Otherwise, the compiler does not generate any output files.</span></span> <span data-ttu-id="6378b-116">Vous devez ensuite compiler les deux fichiers de sortie pour rendre les informations de classe disponibles pour WMI.</span><span class="sxs-lookup"><span data-stu-id="6378b-116">You must then compile the two output files to make the class information available to WMI.</span></span>

 


```mof
#pragma amendment ("MS_409")

[Description("Localized version of MyClass" for American English") :
    Amended, LOCALE(0x409)] 

Class myclass
{
     [DisplayName("User Name") : Amended,
     Description("The Name property contains the name of the user") : 
     Amended, key]
    string Name;

    uint64 Value; // non-localized value field

     [DisplayName("Time Stamp") : Amended,
     Description("This property shows when the object was created") : 
     Amended] 
    uint64 Timestamp;
};
```



## <a name="requirements"></a><span data-ttu-id="6378b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6378b-117">Requirements</span></span>



| <span data-ttu-id="6378b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6378b-118">Requirement</span></span> | <span data-ttu-id="6378b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6378b-119">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="6378b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6378b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6378b-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6378b-121">Windows Vista</span></span><br/>       |
| <span data-ttu-id="6378b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6378b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6378b-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6378b-123">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6378b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6378b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6378b-125">Commandes de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="6378b-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




