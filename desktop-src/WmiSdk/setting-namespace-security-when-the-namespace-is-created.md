---
title: Définition de la sécurité pour la création d’espaces de noms
description: Le fichier format MOF (MOF) qui crée un espace de noms peut également définir les descripteurs de sécurité pour l’espace de noms en incluant le qualificateur NamespaceSecuritySDDL avec le descripteur de sécurité au format SDDL (Security Descriptor Definition Language).
ms.assetid: eeda3351-11ec-4064-90dd-f67ccf5c8cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461b23dbac3984ffdd49311cbe340ae2b0c5b022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530136"
---
# <a name="setting-security-on-namespace-creation"></a><span data-ttu-id="d66b2-103">Définition de la sécurité pour la création d’espaces de noms</span><span class="sxs-lookup"><span data-stu-id="d66b2-103">Setting security on namespace creation</span></span>

<span data-ttu-id="d66b2-104">Le fichier format MOF (MOF) qui crée un espace de noms peut également définir les [*descripteurs de sécurité*](/windows/desktop/SecGloss/s-gly) pour l’espace de noms en incluant le qualificateur **NamespaceSecuritySDDL** avec le descripteur de sécurité au format [SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) .</span><span class="sxs-lookup"><span data-stu-id="d66b2-104">The Managed Object Format (MOF) file that creates a namespace can also define the [*security descriptors*](/windows/desktop/SecGloss/s-gly) for the namespace by including the **NamespaceSecuritySDDL** qualifier with the security descriptor in [security descriptor definition language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) format.</span></span>

<span data-ttu-id="d66b2-105">Vous pouvez utiliser **NamespaceSecuritySDDL** pour sécuriser n’importe quel espace de noms.</span><span class="sxs-lookup"><span data-stu-id="d66b2-105">You can use **NamespaceSecuritySDDL** to secure any namespace.</span></span> <span data-ttu-id="d66b2-106">Vous pouvez également utiliser ce qualificateur dans un simple fichier MOF pour modifier le descripteur de sécurité sur un espace de noms existant.</span><span class="sxs-lookup"><span data-stu-id="d66b2-106">You can also use this qualifier in a simple MOF file to alter the security descriptor on an existing namespace.</span></span> <span data-ttu-id="d66b2-107">La chaîne SDDL est traitée par WMI pour établir la sécurité de l’espace de noms, mais elle n’est pas stockée sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="d66b2-107">The SDDL string is processed by WMI to establish the namespace security but is not stored as a string.</span></span> <span data-ttu-id="d66b2-108">Si aucun descripteur de sécurité n’est spécifié, la sécurité par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="d66b2-108">If no security descriptor is specified, the default security is used.</span></span> <span data-ttu-id="d66b2-109">Pour plus d’informations, consultez [définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="d66b2-109">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

<span data-ttu-id="d66b2-110">La procédure suivante définit le descripteur de sécurité pour l’espace de noms *\\ MyNamespace racine* .</span><span class="sxs-lookup"><span data-stu-id="d66b2-110">The following procedure sets the security descriptor for the *root\\MyNamespace* namespace.</span></span> <span data-ttu-id="d66b2-111">La chaîne SDDL définit le propriétaire et le groupe sur les utilisateurs authentifiés et spécifie une [*liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) qui est héritée par les espaces de noms enfants.</span><span class="sxs-lookup"><span data-stu-id="d66b2-111">The SDDL string sets the owner and group to authenticated users and specifies a [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) that is inherited by child namespaces.</span></span> <span data-ttu-id="d66b2-112">La liste DACL permet à l’utilisateur de lire des données, d’exécuter des méthodes, d’écrire des données dans des classes de fournisseur et d’utiliser l’accès à distance : **WBEM \_ Enable**, **\_ méthode WBEM \_ Execute**, **\_ \_ fournisseur d’écriture WBEM**, **\_ \_ accès à distance WBEM**.</span><span class="sxs-lookup"><span data-stu-id="d66b2-112">The DACL allows the user the right to read data, execute methods, write data to provider classes and use remote access: **WBEM\_ENABLE**, **WBEM\_METHOD\_EXECUTE**, **WBEM\_WRITE\_PROVIDER**, **WBEM\_REMOTE\_ACCESS**.</span></span> <span data-ttu-id="d66b2-113">Pour plus d’informations, consultez [accès aux espaces de noms WMI](access-to-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="d66b2-113">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="d66b2-114">**Pour définir une liste DACL d’espace de noms**</span><span class="sxs-lookup"><span data-stu-id="d66b2-114">**To set a namespace DACL**</span></span>

1.  <span data-ttu-id="d66b2-115">Créez un fichier format MOF (MOF) ou modifiez votre fichier MOF existant qui définit l’espace de noms pour ajouter le qualificateur **NamespaceSecuritySDDL** à la chaîne SDDL.</span><span class="sxs-lookup"><span data-stu-id="d66b2-115">Create a Managed Object Format (MOF) file or modify your existing MOF file that defines the namespace to add the **NamespaceSecuritySDDL** qualifier with the SDDL string.</span></span>

    <span data-ttu-id="d66b2-116">L’exemple de code suivant montre que l’espace de noms à modifier est root \\ MyNamespace et que le fichier est nommé MyNamespace \_ Security. mof.</span><span class="sxs-lookup"><span data-stu-id="d66b2-116">The following code example shows the namespace to be modified is root\\MyNamespace and the file is named MyNamespace\_security.mof.</span></span>

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL ("O:BAG:BAD:(A;CI;0x60003;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

2.  <span data-ttu-id="d66b2-117">Sachez que la chaîne SDDL respecte la casse : les lettres doivent être en majuscules.</span><span class="sxs-lookup"><span data-stu-id="d66b2-117">Be aware that the SDDL string is case-sensitive: the letters must be capitalized.</span></span>

    <span data-ttu-id="d66b2-118">L’exemple de code suivant affiche les lettres « o » et « g » dans la chaîne SDDL en minuscules et génère une erreur Mofcomp.exe.</span><span class="sxs-lookup"><span data-stu-id="d66b2-118">The following code example shows the letters "o" and "g" in the SDDL string as lowercase and will cause Mofcomp.exe to return an error.</span></span>

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL("o:BAg:BAD:(A;CI;0x60003;;;WD)")] 
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

3.  <span data-ttu-id="d66b2-119">Exécutez [**Mofcomp.exe**](mofcomp.md) pour compiler le fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="d66b2-119">Run [**Mofcomp.exe**](mofcomp.md) to compile the MOF file.</span></span>

    <span data-ttu-id="d66b2-120">**c : \\ mofcomp MyNamespace \_ Security. mof**</span><span class="sxs-lookup"><span data-stu-id="d66b2-120">**c:\\mofcomp MyNamespace\_security.mof**</span></span>

    <span data-ttu-id="d66b2-121">En C++, utilisez les méthodes [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="d66b2-121">In C++, use the [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) methods.</span></span>

4.  <span data-ttu-id="d66b2-122">Si votre tentative de définition de la liste DACL d’espace de noms échoue, examinez les messages d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="d66b2-122">If your attempt to set the namespace DACL fails, consider the following error messages:</span></span>

    

    | <span data-ttu-id="d66b2-123">Error</span><span class="sxs-lookup"><span data-stu-id="d66b2-123">Error</span></span>                           | <span data-ttu-id="d66b2-124">Description</span><span class="sxs-lookup"><span data-stu-id="d66b2-124">Description</span></span>                                                                                                  |
    |---------------------------------|--------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="d66b2-125">**\_paramètre WBEM E \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d66b2-125">**WBEM\_E\_INVALID\_PARAMETER**</span></span> | <span data-ttu-id="d66b2-126">Il n’y a aucune DACL héritée.</span><span class="sxs-lookup"><span data-stu-id="d66b2-126">There is no inherited DACL.</span></span> <span data-ttu-id="d66b2-127">Sinon, l’appelant n’a pas respecté la liste DACL ou le SD dans l’espace de noms parent.</span><span class="sxs-lookup"><span data-stu-id="d66b2-127">Alternately, the caller has violated the DACL or the SD in the parent namespace.</span></span> |
    | <span data-ttu-id="d66b2-128">**\_accès WBEM \_ E \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="d66b2-128">**WBEM\_E\_ACCESS\_DENIED**</span></span>     | <span data-ttu-id="d66b2-129">L’appelant n’est pas autorisé à mettre à jour le SDDL dans MOF.</span><span class="sxs-lookup"><span data-stu-id="d66b2-129">The caller does not have permission to update the SDDL in MOF.</span></span>                                               |

    

     

## <a name="related-topics"></a><span data-ttu-id="d66b2-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d66b2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d66b2-131">Définition des descripteurs de sécurité des espaces de noms</span><span class="sxs-lookup"><span data-stu-id="d66b2-131">Setting Namespace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="d66b2-132">**Constantes de droits d’accès à l’espace de noms**</span><span class="sxs-lookup"><span data-stu-id="d66b2-132">**Namespace Access Rights Constants**</span></span>](namespace-access-rights-constants.md)
</dt> <dt>

[<span data-ttu-id="d66b2-133">**Constantes d’indicateur ACE d’espace de noms**</span><span class="sxs-lookup"><span data-stu-id="d66b2-133">**Namespace ACE Flag Constants**</span></span>](namespace-ace-flag-constants.md)
</dt> <dt>

[<span data-ttu-id="d66b2-134">Modification de la sécurité d’accès sur les objets sécurisables</span><span class="sxs-lookup"><span data-stu-id="d66b2-134">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
