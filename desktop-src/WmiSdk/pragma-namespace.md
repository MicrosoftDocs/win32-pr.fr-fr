---
description: Demande que le compilateur charge le fichier MOF dans l’espace de noms spécifié en tant que NamespacePath. Si le commutateur d’espace de noms MOF compiler-n et l' \# espace de noms pragma&\# 32 ; NamespacePath sont utilisés, la commande prend la priorité sur le commutateur.
ms.assetid: d280f67a-a798-47c0-b8de-071c290dd216
ms.tgt_platform: multiple
title: espace de noms pragma
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
ms.openlocfilehash: b5f5e164632fef5a41e7233caf4fd154d1dafe16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753685"
---
# <a name="pragma-namespace"></a><span data-ttu-id="2230f-104">espace de noms pragma</span><span class="sxs-lookup"><span data-stu-id="2230f-104">pragma namespace</span></span>

<span data-ttu-id="2230f-105">La commande de préprocesseur d' **espace de noms pragma** demande que le compilateur charge le fichier MOF dans l’espace de noms spécifié en tant que *NamespacePath*.</span><span class="sxs-lookup"><span data-stu-id="2230f-105">The **pragma namespace** preprocessor command requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span> <span data-ttu-id="2230f-106">Si le commutateur d’espace de noms MOF compiler **-n** et la commande **\# pragma namespace** *NamespacePath* sont utilisés, la commande prend la priorité sur le commutateur.</span><span class="sxs-lookup"><span data-stu-id="2230f-106">If both the MOF compiler **-n** namespace switch and the **\#pragma namespace** *namespacepath* command are used, the command takes priority over the switch.</span></span>

<span data-ttu-id="2230f-107">Les éléments suivants décrivent la syntaxe :</span><span class="sxs-lookup"><span data-stu-id="2230f-107">The following describes the syntax:</span></span>


```mof
#pragma namespace ("[Namespace]")
```



<span data-ttu-id="2230f-108">L' *\[ espace de noms \]* est l’espace de noms spécifié.</span><span class="sxs-lookup"><span data-stu-id="2230f-108">*\[Namespace\]* is the specified namespace.</span></span>

<span data-ttu-id="2230f-109">Si vous ne spécifiez pas cette commande ou le commutateur de ligne de commande équivalent, le compilateur MOF utilise par \\ défaut l’espace de noms racine par défaut.</span><span class="sxs-lookup"><span data-stu-id="2230f-109">If you do not specify this command or the equivalent command-line switch, the MOF compiler uses the root\\default namespace by default.</span></span>

## <a name="remarks"></a><span data-ttu-id="2230f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="2230f-110">Remarks</span></span>

<span data-ttu-id="2230f-111">Vous pouvez exiger que les applications et les scripts clients utilisent une connexion chiffrée pour l’authentification en ajoutant le qualificateur **RequiresEncryption** au fichier. MOF qui crée l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="2230f-111">You can require that client scripts and applications use an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the .mof file that creates the namespace.</span></span> <span data-ttu-id="2230f-112">Vous pouvez également modifier un espace de noms existant en ajoutant cet attribut et recompiler le fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="2230f-112">You can also modify an existing namespace by adding this attribute and compile the MOF file again.</span></span> <span data-ttu-id="2230f-113">Pour plus d’informations sur l’utilisation de **RequiresEncryption**, consultez la page [exiger une connexion chiffrée à un espace de noms](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="2230f-113">For more information about how to use **RequiresEncryption**, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2230f-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="2230f-114">Examples</span></span>

<span data-ttu-id="2230f-115">L’exemple suivant montre comment placer des classes ou des instances dans l' \\ espace de noms « test racine ».</span><span class="sxs-lookup"><span data-stu-id="2230f-115">The following example shows how place classes or instances in the "Root\\Test" namespace.</span></span>


```mof
#pragma namespace ("\\\\.\\Root\\Test")
```



## <a name="requirements"></a><span data-ttu-id="2230f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2230f-116">Requirements</span></span>



| <span data-ttu-id="2230f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2230f-117">Requirement</span></span> | <span data-ttu-id="2230f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="2230f-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="2230f-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2230f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2230f-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2230f-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="2230f-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2230f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2230f-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2230f-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2230f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2230f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2230f-124">Définition des descripteurs de sécurité espace</span><span class="sxs-lookup"><span data-stu-id="2230f-124">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="2230f-125">**Qualificateurs WMI standard**</span><span class="sxs-lookup"><span data-stu-id="2230f-125">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="2230f-126">Commandes de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="2230f-126">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




