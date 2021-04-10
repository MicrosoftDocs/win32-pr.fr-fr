---
title: Création de groupes dans un domaine
description: Un objet de groupe est créé dans Active Directory Domain Services dans le conteneur de domaine où sera contenu le nouveau groupe.
ms.assetid: 40792878-4219-4242-8cf7-b092b28f2ff4
ms.tgt_platform: multiple
keywords:
- groupes Active Directory, création de groupes dans un domaine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100700b08fb82b750ee68dfed6bcb26060929e87
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031030"
---
# <a name="creating-groups-in-a-domain"></a><span data-ttu-id="3fba1-104">Création de groupes dans un domaine</span><span class="sxs-lookup"><span data-stu-id="3fba1-104">Creating Groups in a Domain</span></span>

<span data-ttu-id="3fba1-105">Un objet de groupe est créé dans Active Directory Domain Services dans le conteneur de domaine où sera contenu le nouveau groupe.</span><span class="sxs-lookup"><span data-stu-id="3fba1-105">A group object is created in Active Directory Domain Services in the domain container where the new group will be contained.</span></span> <span data-ttu-id="3fba1-106">Les groupes peuvent être créés à la racine du domaine, au sein d’une unité d’organisation ou au sein d’un conteneur.</span><span class="sxs-lookup"><span data-stu-id="3fba1-106">Groups can be created at the root of the domain, within an organizational unit, or within a container.</span></span> <span data-ttu-id="3fba1-107">Pour créer un objet de groupe, utilisez la méthode [**IADsContainer :: Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) ou [**IDirectoryObject :: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) .</span><span class="sxs-lookup"><span data-stu-id="3fba1-107">To create a group object, use the [**IADsContainer::Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) or the [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) method.</span></span>

<span data-ttu-id="3fba1-108">Les attributs suivants sont requis pour que l’objet groupe soit un groupe juridique que le serveur Active Directory et le système de sécurité Windows reconnaissent :</span><span class="sxs-lookup"><span data-stu-id="3fba1-108">The following attributes are required to make the group object a legal group that the Active Directory server and the Windows security system will recognize:</span></span>

<dl> <dt>

<span data-ttu-id="3fba1-109"><span id="cn"></span><span id="CN"></span>**8525**</span><span class="sxs-lookup"><span data-stu-id="3fba1-109"><span id="cn"></span><span id="CN"></span>**cn**</span></span>
</dt> <dd>

<span data-ttu-id="3fba1-110">Spécifie le nom de l’objet de groupe dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="3fba1-110">Specifies the name of the group object in the directory.</span></span> <span data-ttu-id="3fba1-111">Il s’agit du nom unique relatif de l’objet dans le conteneur où le groupe est créé.</span><span class="sxs-lookup"><span data-stu-id="3fba1-111">This will be the object's relative distinguished name within the container where the group is created.</span></span>

</dd> <dt>

<span data-ttu-id="3fba1-112"><span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**groupType**</span><span class="sxs-lookup"><span data-stu-id="3fba1-112"><span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**groupType**</span></span>
</dt> <dd>

<span data-ttu-id="3fba1-113">Contient un entier qui spécifie le type de groupe et la portée.</span><span class="sxs-lookup"><span data-stu-id="3fba1-113">Contains an integer that specifies the group type and scope.</span></span> <span data-ttu-id="3fba1-114">L’énumération [**enum de \_ type de groupe \_ \_ ADS**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) définit les valeurs possibles pour l’attribut **GroupType** .</span><span class="sxs-lookup"><span data-stu-id="3fba1-114">The [**ADS\_GROUP\_TYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) enumeration defines the possible values for the **groupType** attribute.</span></span>

<span data-ttu-id="3fba1-115">La liste suivante définit les types et les valeurs de groupes communs pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="3fba1-115">The following list defines common group types and values for this attribute.</span></span>

<dl> <dt>

<span data-ttu-id="3fba1-116"><span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Distribution locale de domaine</span><span class="sxs-lookup"><span data-stu-id="3fba1-116"><span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Domain Local Distribution</span></span>
</dt> <dd>

<span data-ttu-id="3fba1-117">**\_type de groupe ad \_ \_ groupe de domaine \_ local \_**</span><span class="sxs-lookup"><span data-stu-id="3fba1-117">**ADS\_GROUP\_TYPE\_DOMAIN\_LOCAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="3fba1-118"><span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Sécurité locale du domaine</span><span class="sxs-lookup"><span data-stu-id="3fba1-118"><span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Domain Local Security</span></span>
</dt> <dd>

<span data-ttu-id="3fba1-119">**Annonces \_ type de groupe \_ \_ domaine \_ local \_ groupe** ad groupe de groupes \| **annonces \_ \_ \_ sécurité \_ activée**</span><span class="sxs-lookup"><span data-stu-id="3fba1-119">**ADS\_GROUP\_TYPE\_DOMAIN\_LOCAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>

<span data-ttu-id="3fba1-120"><span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Distribution mondiale</span><span class="sxs-lookup"><span data-stu-id="3fba1-120"><span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Global Distribution</span></span>
</dt> <dd>

<span data-ttu-id="3fba1-121">**\_ \_ groupe global du type de groupe ADS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3fba1-121">**ADS\_GROUP\_TYPE\_GLOBAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="3fba1-122"><span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Sécurité globale</span><span class="sxs-lookup"><span data-stu-id="3fba1-122"><span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Global Security</span></span>
</dt> <dd>

<span data-ttu-id="3fba1-123">**Annonces \_ type de groupe groupes \_ \_ globaux \_** \| **ad groupe annonces \_ \_ \_ sécurité \_ activée**</span><span class="sxs-lookup"><span data-stu-id="3fba1-123">**ADS\_GROUP\_TYPE\_GLOBAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>

<span data-ttu-id="3fba1-124"><span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Distribution universelle</span><span class="sxs-lookup"><span data-stu-id="3fba1-124"><span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Universal Distribution</span></span>
</dt> <dd>

<span data-ttu-id="3fba1-125">**\_ \_ groupe universel de type groupe \_ ad \_**</span><span class="sxs-lookup"><span data-stu-id="3fba1-125">**ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="3fba1-126"><span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Sécurité universelle</span><span class="sxs-lookup"><span data-stu-id="3fba1-126"><span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Universal Security</span></span>
</dt> <dd>

<span data-ttu-id="3fba1-127">**Annonces \_ \_type de \_ \_** groupe annonces de groupe universel sécurité de type de groupe \| **\_ \_ \_ \_ activée**</span><span class="sxs-lookup"><span data-stu-id="3fba1-127">**ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>


</dt> <dd>

</dd> </dl>

<span data-ttu-id="3fba1-128">Si le groupe est conçu pour définir le contrôle d’accès sur les objets d’annuaire, le groupe doit être un groupe de sécurité global ou universel.</span><span class="sxs-lookup"><span data-stu-id="3fba1-128">If the group is intended for setting access control on directory objects, the group should be a Global Security or Universal Security group.</span></span>

<span data-ttu-id="3fba1-129">Sachez que les groupes de sécurité universels ne peuvent être créés que sur des domaines Windows 2000 s’exécutant en mode natif.</span><span class="sxs-lookup"><span data-stu-id="3fba1-129">Be aware that Universal Security groups can only be created on Windows 2000 domains running in native mode.</span></span> <span data-ttu-id="3fba1-130">Pour plus d’informations sur la détection du mode mixte et le mode natif, consultez [détection du mode d’opération d’un domaine](detecting-the-operation-mode-of-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="3fba1-130">For more information about detecting mixed and native mode, see [Detecting the Operation Mode of a Domain](detecting-the-operation-mode-of-a-domain.md).</span></span>

</dd> <dt>

<span data-ttu-id="3fba1-131"><span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**sAMAccountName**</span><span class="sxs-lookup"><span data-stu-id="3fba1-131"><span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**sAMAccountName**</span></span>
</dt> <dd>

<span data-ttu-id="3fba1-132">Contient une chaîne qui est le nom utilisé pour prendre en charge les clients et les serveurs d’une version précédente.</span><span class="sxs-lookup"><span data-stu-id="3fba1-132">Contains a string that is the name used to support clients and servers from a previous version.</span></span> <span data-ttu-id="3fba1-133">Le **sAMAccountName** doit comporter moins de 20 caractères pour prendre en charge les clients d’une version précédente de Windows.</span><span class="sxs-lookup"><span data-stu-id="3fba1-133">The **sAMAccountName** should be less than 20 characters to support clients of a previous version of Windows.</span></span>

<span data-ttu-id="3fba1-134">**SAMAccountName** doit être unique parmi tous les objets principaux de sécurité au sein du domaine.</span><span class="sxs-lookup"><span data-stu-id="3fba1-134">The **sAMAccountName** must be unique among all security principal objects within the domain.</span></span> <span data-ttu-id="3fba1-135">Une requête doit être exécutée sur le domaine pour vérifier que le **sAMAccountName** est unique au sein du domaine.</span><span class="sxs-lookup"><span data-stu-id="3fba1-135">A query should be performed against the domain to verify that the **sAMAccountName** is unique within the domain.</span></span>

</dd> </dl>

<span data-ttu-id="3fba1-136">Les membres du groupe peuvent être ajoutés au moment de la création à l’aide de la méthode [**IDirectoryObject :: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) .</span><span class="sxs-lookup"><span data-stu-id="3fba1-136">The members of the group can be added at creation time using the [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) method.</span></span> <span data-ttu-id="3fba1-137">Si vous le souhaitez, des membres peuvent être ajoutés au groupe après la création à l’aide de la méthode [**IADsGroup :: Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) .</span><span class="sxs-lookup"><span data-stu-id="3fba1-137">Optionally, members can be added to the group after creation using the [**IADsGroup::Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) method.</span></span> <span data-ttu-id="3fba1-138">Pour plus d’informations sur l’ajout de membres à un groupe, consultez [Ajout de membres à des groupes dans un domaine](adding-members-to-groups-in-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="3fba1-138">For more information about adding members to a group, see [Adding Members to Groups in a Domain](adding-members-to-groups-in-a-domain.md).</span></span>

 

 