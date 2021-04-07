---
title: Comment étendre le schéma
description: Lorsque les classes et/ou les attributs existants ne correspondent pas au type de données que vous souhaitez stocker, vous pouvez étendre le schéma.
ms.assetid: 9a80ce29-8ff0-4324-8a2f-afd6c5d2272e
ms.tgt_platform: multiple
keywords:
- Schéma AD, comment étendre
- Active Directory, utilisation de, schéma
- Active Directory, utiliser, schéma, étendre le schéma, comment étendre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437b23229182e6ec6f94b500feb764b4bbcf06e7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724493"
---
# <a name="how-to-extend-the-schema"></a><span data-ttu-id="66d1d-106">Comment étendre le schéma</span><span class="sxs-lookup"><span data-stu-id="66d1d-106">How to Extend the Schema</span></span>

<span data-ttu-id="66d1d-107">Lorsque les classes et/ou les attributs existants ne correspondent pas au type de données que vous souhaitez stocker, vous pouvez étendre le schéma.</span><span class="sxs-lookup"><span data-stu-id="66d1d-107">When the existing classes and/or attributes do not fit with the type of data that you want to store, you might want to extend the schema.</span></span> <span data-ttu-id="66d1d-108">Pour plus d’informations sur le choix de l’extension du schéma, consultez [extension du schéma](extending-the-schema.md).</span><span class="sxs-lookup"><span data-stu-id="66d1d-108">For more information on deciding when to extend the schema, see [Extending the Schema](extending-the-schema.md).</span></span> <span data-ttu-id="66d1d-109">Lorsque vous avez décidé que l’extension de schéma est requise, utilisez la procédure suivante pour étendre le schéma.</span><span class="sxs-lookup"><span data-stu-id="66d1d-109">When you have decided that schema extension is required, use the following procedure to extend the schema.</span></span>

## <a name="verify-active-directory-functionality-before-you-apply-any-schema-extensions"></a><span data-ttu-id="66d1d-110">Vérifier Active Directory fonctionnalité avant d’appliquer des extensions de schéma</span><span class="sxs-lookup"><span data-stu-id="66d1d-110">Verify Active Directory functionality before you apply any schema extensions</span></span>

<span data-ttu-id="66d1d-111">Vérifiez Active Directory fonctionnalité avant de mettre à jour le schéma pour vous assurer que l’extension de schéma continue sans erreur.</span><span class="sxs-lookup"><span data-stu-id="66d1d-111">Verify Active Directory functionality before you update the schema to help ensure that the schema extension proceeds without error.</span></span> <span data-ttu-id="66d1d-112">Au minimum, assurez-vous que tous les contrôleurs de domaine de la forêt sont en ligne et qu’ils effectuent une réplication entrante.</span><span class="sxs-lookup"><span data-stu-id="66d1d-112">At a minimum, ensure that all domain controllers for the forest are online and performing inbound replication.</span></span>

<span data-ttu-id="66d1d-113">**Pour vérifier Active Directory fonctionnalité avant d’appliquer l’extension de schéma**</span><span class="sxs-lookup"><span data-stu-id="66d1d-113">**To verify Active Directory functionality before you apply the schema extension**</span></span>

1.  <span data-ttu-id="66d1d-114">Connectez-vous à une station de travail d’administration sur laquelle l’outil de support Windows Repadmin.exe installé.</span><span class="sxs-lookup"><span data-stu-id="66d1d-114">Log on to an administrative workstation that has the Windows Support Tool Repadmin.exe installed.</span></span>
    > [!Note]  
    > <span data-ttu-id="66d1d-115">Les outils de support sont situés sur le support d’installation du système d’exploitation dans le \\ dossier Outils de support.</span><span class="sxs-lookup"><span data-stu-id="66d1d-115">The Support Tools are located on the operating system installation media in the Support\\Tools folder.</span></span>

     

2.  <span data-ttu-id="66d1d-116">Ouvrez une invite de commandes, puis accédez au dossier dans lequel les outils de support Windows sont installés.</span><span class="sxs-lookup"><span data-stu-id="66d1d-116">Open a command prompt, and then change directories to the folder in which the Windows Support Tools are installed.</span></span>
3.  <span data-ttu-id="66d1d-117">À une invite de commandes, tapez ce qui suit puis appuyez sur ENTRÉE :</span><span class="sxs-lookup"><span data-stu-id="66d1d-117">At a command prompt, type the following, and then press ENTER:</span></span>

    ``` syntax
    repadmin /replsum /bysrc /bydest /sort:delta
    ```

    <span data-ttu-id="66d1d-118">Tous les contrôleurs de domaine doivent afficher la valeur 0 dans la colonne échecs et les deltas les plus importants (qui indiquent le nombre de modifications apportées à la base de données Active Directory depuis la dernière réplication réussie) doivent être inférieurs ou approximativement à la fréquence de réplication du lien de site utilisé par le contrôleur de domaine pour la réplication.</span><span class="sxs-lookup"><span data-stu-id="66d1d-118">All domain controllers should show 0 in the Fails column, and the largest deltas (which indicate the number of changes that have been made to the Active Directory database since the last successful replication) should be less than or roughly equal to the replication frequency of the site link that is used by the domain controller for replication.</span></span> <span data-ttu-id="66d1d-119">La fréquence de réplication par défaut est de 180 minutes.</span><span class="sxs-lookup"><span data-stu-id="66d1d-119">The default replication frequency is 180 minutes.</span></span>

    <span data-ttu-id="66d1d-120">Pour plus d’informations sur les étapes supplémentaires que vous pouvez suivre pour vérifier Active Directory fonctionnalités avant d’appliquer l’extension de schéma, consultez [l’article 325379 de la base de connaissances Microsoft](https://support.microsoft.com/kb/325379/en-us).</span><span class="sxs-lookup"><span data-stu-id="66d1d-120">For more information about additional steps that you can take to verify Active Directory functionality before you apply the schema extension, see [article 325379 in the Microsoft Knowledge Base](https://support.microsoft.com/kb/325379/en-us).</span></span>

<span data-ttu-id="66d1d-121">**Pour étendre le schéma**</span><span class="sxs-lookup"><span data-stu-id="66d1d-121">**To Extend the Schema**</span></span>

1.  <span data-ttu-id="66d1d-122">Déterminez la méthode de l’extension.</span><span class="sxs-lookup"><span data-stu-id="66d1d-122">Determine the method of extension.</span></span> <span data-ttu-id="66d1d-123">Une fois que vous avez soigneusement conçu vos modifications de schéma, l’étape suivante consiste à choisir la méthode à utiliser pour étendre le schéma.</span><span class="sxs-lookup"><span data-stu-id="66d1d-123">Once you have carefully designed your schema changes, the next step is to decide which method to use to extend the schema.</span></span> <span data-ttu-id="66d1d-124">Vous pouvez utiliser l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="66d1d-124">You can use one of the following methods:</span></span>
    -   <span data-ttu-id="66d1d-125">Manuellement, à l’aide des fichiers d’importation.</span><span class="sxs-lookup"><span data-stu-id="66d1d-125">Manually, using import files.</span></span> <span data-ttu-id="66d1d-126">Consultez la documentation [à l’aide de l’outil LDIFDE](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65)).</span><span class="sxs-lookup"><span data-stu-id="66d1d-126">See the documentation [Using the LDIFDE Tool](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65)).</span></span>
        > [!Note]  
        > <span data-ttu-id="66d1d-127">N’utilisez pas LDIFDE pour importer des fichiers Windows SCH \* . ldf.</span><span class="sxs-lookup"><span data-stu-id="66d1d-127">Do not use LDIFDE to import Windows Sch\*.ldf files.</span></span> <span data-ttu-id="66d1d-128">Ces fichiers sont requis pour étendre le schéma de Active Directory afin d’installer des contrôleurs de domaine qui exécutent une version plus récente de Windows Server que la version exécutée sur le contrôleur de schéma actuel.</span><span class="sxs-lookup"><span data-stu-id="66d1d-128">Those files are required to extend the Active Directory schema in order to install domain controllers that run a newer version of Windows Server than the version that is running on the current schema master.</span></span> <span data-ttu-id="66d1d-129">Lorsque vous avez besoin d’étendre le schéma pour installer un nouveau contrôleur de domaine, utilisez Adprep.exe.</span><span class="sxs-lookup"><span data-stu-id="66d1d-129">When you need to extend the schema in order to install a new domain controller, use Adprep.exe.</span></span>

         

    -   <span data-ttu-id="66d1d-130">Par programmation, à l’aide d’un programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="66d1d-130">Programmatically, using an installation program.</span></span> <span data-ttu-id="66d1d-131">Pour plus d’informations, consultez [extension par programmation](programmatic-extension.md)</span><span class="sxs-lookup"><span data-stu-id="66d1d-131">For more information, see [Programmatic Extension](programmatic-extension.md)</span></span>
2.  <span data-ttu-id="66d1d-132">Activer les modifications de schéma.</span><span class="sxs-lookup"><span data-stu-id="66d1d-132">Enable Schema Changes.</span></span> <span data-ttu-id="66d1d-133">Pour plus d’informations, consultez [Configuration requise pour l’installation d’une extension de schéma](prerequisites-for-installing-a-schema-extension.md) et [activation des modifications de schéma sur le contrôleur de schéma](enabling-schema-changes-at-the-schema-master.md).</span><span class="sxs-lookup"><span data-stu-id="66d1d-133">For more information, see [Prerequisites for Installing a Schema Extension](prerequisites-for-installing-a-schema-extension.md) and [Enabling Schema Changes at the Schema Master](enabling-schema-changes-at-the-schema-master.md).</span></span>
3.  <span data-ttu-id="66d1d-134">Obtenez un identificateur d’objet (OID) pour vos nouveaux attributs et/ou classes, comme décrit dans [obtention d’un identificateur d’objet](obtaining-an-object-identifier.md).</span><span class="sxs-lookup"><span data-stu-id="66d1d-134">Obtain an Object Identifier (OID) for your new attributes and/or classes, as described in [Obtaining an Object Identifier](obtaining-an-object-identifier.md).</span></span>
4.  <span data-ttu-id="66d1d-135">Créer des attributs et des classes.</span><span class="sxs-lookup"><span data-stu-id="66d1d-135">Create new attributes and classes.</span></span>
5.  <span data-ttu-id="66d1d-136">Utilisez les spécificateurs d’affichage pour intégrer de nouveaux attributs et classes à l’interface utilisateur, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="66d1d-136">Use display specifiers to integrate new attributes and classes with the user interface, if necessary.</span></span>
6.  <span data-ttu-id="66d1d-137">Mettez à jour le cache de schéma comme décrit dans [mise à jour du cache de schéma](updating-the-schema-cache.md).</span><span class="sxs-lookup"><span data-stu-id="66d1d-137">Update the schema cache as described in [Updating the Schema Cache](updating-the-schema-cache.md).</span></span>
7.  <span data-ttu-id="66d1d-138">Vérifiez l’extension de schéma à l’aide de LDP.exe.</span><span class="sxs-lookup"><span data-stu-id="66d1d-138">Verify the schema extension using LDP.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66d1d-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="66d1d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66d1d-140">Obtention d’un identificateur d’objet</span><span class="sxs-lookup"><span data-stu-id="66d1d-140">Obtaining an Object Identifier</span></span>](obtaining-an-object-identifier.md)
</dt> <dt>

[<span data-ttu-id="66d1d-141">Les nouveaux outils en ligne de commande pour Active Directory dans Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="66d1d-141">The new command-line tools for Active Directory in Windows Server 2003</span></span>](https://support.microsoft.com/kb/298882)
</dt> <dt>

<span data-ttu-id="66d1d-142">[Utilisation de l’outil LDIFDE](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))</span><span class="sxs-lookup"><span data-stu-id="66d1d-142">[Using the LDIFDE Tool](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))</span></span>
</dt> <dt>

<span data-ttu-id="66d1d-143">[Extension du schéma Active Directory](/previous-versions/ms806972(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="66d1d-143">[Extending the Active Directory Schema](/previous-versions/ms806972(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="66d1d-144">Restrictions sur l’extension de schéma</span><span class="sxs-lookup"><span data-stu-id="66d1d-144">Restrictions on Schema Extension</span></span>](restrictions-on-schema-extension.md)
</dt> </dl>

 

 