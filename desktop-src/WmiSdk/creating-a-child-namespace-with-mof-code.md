---
description: Le moyen le plus simple de créer un espace de noms consiste à utiliser du code format MOF (MOF) pour créer l’espace de noms dans le répertoire actif. Le répertoire actif est défini lorsque vous vous connectez.
ms.assetid: 2b83cd96-079f-4178-9e5a-68ede3a92066
ms.tgt_platform: multiple
title: Création d’un espace de noms enfant avec du code MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f80aa04e2ef4f5c7bbfc43d9020727b3b2a6e0d
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104042972"
---
# <a name="creating-a-child-namespace-with-mof-code"></a><span data-ttu-id="ecaf6-104">Création d’un espace de noms enfant avec du code MOF</span><span class="sxs-lookup"><span data-stu-id="ecaf6-104">Creating a Child Namespace with MOF Code</span></span>

<span data-ttu-id="ecaf6-105">Le moyen le plus simple de créer un espace de noms consiste à utiliser du code format MOF (MOF) pour créer l’espace de noms dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="ecaf6-105">The simplest way of creating a namespace is to use Managed Object Format (MOF) code to create the namespace inside the current directory.</span></span> <span data-ttu-id="ecaf6-106">Le répertoire actif est défini lorsque vous vous connectez.</span><span class="sxs-lookup"><span data-stu-id="ecaf6-106">The current directory is defined when you log on.</span></span>

<span data-ttu-id="ecaf6-107">La procédure suivante décrit comment créer un espace de noms enfant à l’aide de code MOF.</span><span class="sxs-lookup"><span data-stu-id="ecaf6-107">The following procedure describes how to create a child namespace using MOF code.</span></span>

<span data-ttu-id="ecaf6-108">**Pour créer un espace de noms enfant à l’aide du code MOF**</span><span class="sxs-lookup"><span data-stu-id="ecaf6-108">**To create a child namespace using MOF code**</span></span>

1.  <span data-ttu-id="ecaf6-109">Créez une instance de la classe d' [**\_ \_ espace de noms**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="ecaf6-109">Create an instance of the [**\_\_Namespace**](--namespace.md) class.</span></span>

    <span data-ttu-id="ecaf6-110">L’exemple de code suivant montre comment créer un espace de noms enfant.</span><span class="sxs-lookup"><span data-stu-id="ecaf6-110">The following code example shows how to create a child namespace.</span></span>

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
    };
    ```

2.  <span data-ttu-id="ecaf6-111">Si vous souhaitez exiger de l’utilisateur qu’il établisse une connexion chiffrée à l’espace de noms, utilisez le qualificateur **RequiresEncryption** .</span><span class="sxs-lookup"><span data-stu-id="ecaf6-111">If you want to require the user to make an encrypted connection to the namespace, use the **RequiresEncryption** qualifier.</span></span> <span data-ttu-id="ecaf6-112">Pour plus d’informations, consultez [la page exiger une connexion chiffrée à un espace de noms](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="ecaf6-112">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

    <span data-ttu-id="ecaf6-113">L’exemple de code suivant montre comment exiger une connexion chiffrée.</span><span class="sxs-lookup"><span data-stu-id="ecaf6-113">The following code example shows how to require an encrypted connection.</span></span>

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
        [RequiresEncryption(TRUE)] 
        instance of __MyNamespace { };
    };
    ```

3.  <span data-ttu-id="ecaf6-114">Si vous souhaitez définir un descripteur de sécurité sur l’espace de noms plutôt que d’utiliser la sécurité par défaut de l’espace de noms, utilisez le qualificateur **NamespaceSecuritySDDL** .</span><span class="sxs-lookup"><span data-stu-id="ecaf6-114">If you want to set a security descriptor on the namespace rather than using the default namespace security, use the **NamespaceSecuritySDDL** qualifier.</span></span> <span data-ttu-id="ecaf6-115">Pour plus d’informations, consultez [définition de la sécurité de l’espace de noms lors de la création de l’espace de noms](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="ecaf6-115">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>

    <span data-ttu-id="ecaf6-116">L’exemple de code suivant montre comment définir un descripteur de sécurité sur l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="ecaf6-116">The following code example shows how to set a security descriptor on the namespace.</span></span>

    ``` syntax
    #pragma namespace("\\\\.\\root\\MyNamespace")

    [NamespaceSecuritySDDL ("O:AUG:AUD:(A;CI;0x00060033;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

4.  <span data-ttu-id="ecaf6-117">Compilez et chargez l’instance d' [**\_ \_ espace de noms**](--namespace.md) à l’aide de l’utilitaire [mofcomp](mofcomp.md) ou de l’interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="ecaf6-117">Compile and load the [**\_\_Namespace**](--namespace.md) instance using the [mofcomp](mofcomp.md) utility or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span> <span data-ttu-id="ecaf6-118">Mofcomp et l’interface **IMofCompiler** chargent automatiquement l’espace de noms dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="ecaf6-118">Both mofcomp and the **IMofCompiler** interface automatically load the namespace into the current directory.</span></span> <span data-ttu-id="ecaf6-119">Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="ecaf6-119">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ecaf6-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ecaf6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecaf6-121">**Qualificateurs WMI standard**</span><span class="sxs-lookup"><span data-stu-id="ecaf6-121">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> </dl>

 

 



