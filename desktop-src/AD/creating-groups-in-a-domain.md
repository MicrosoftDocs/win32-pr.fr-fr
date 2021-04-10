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
# <a name="creating-groups-in-a-domain"></a>Création de groupes dans un domaine

Un objet de groupe est créé dans Active Directory Domain Services dans le conteneur de domaine où sera contenu le nouveau groupe. Les groupes peuvent être créés à la racine du domaine, au sein d’une unité d’organisation ou au sein d’un conteneur. Pour créer un objet de groupe, utilisez la méthode [**IADsContainer :: Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) ou [**IDirectoryObject :: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) .

Les attributs suivants sont requis pour que l’objet groupe soit un groupe juridique que le serveur Active Directory et le système de sécurité Windows reconnaissent :

<dl> <dt>

<span id="cn"></span><span id="CN"></span>**8525**
</dt> <dd>

Spécifie le nom de l’objet de groupe dans le répertoire. Il s’agit du nom unique relatif de l’objet dans le conteneur où le groupe est créé.

</dd> <dt>

<span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**groupType**
</dt> <dd>

Contient un entier qui spécifie le type de groupe et la portée. L’énumération [**enum de \_ type de groupe \_ \_ ADS**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) définit les valeurs possibles pour l’attribut **GroupType** .

La liste suivante définit les types et les valeurs de groupes communs pour cet attribut.

<dl> <dt>

<span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Distribution locale de domaine
</dt> <dd>

**\_type de groupe ad \_ \_ groupe de domaine \_ local \_**

</dd> <dt>

<span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Sécurité locale du domaine
</dt> <dd>

**Annonces \_ type de groupe \_ \_ domaine \_ local \_ groupe** ad groupe de groupes \| **annonces \_ \_ \_ sécurité \_ activée**

</dd> <dt>

<span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Distribution mondiale
</dt> <dd>

**\_ \_ groupe global du type de groupe ADS \_ \_**

</dd> <dt>

<span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Sécurité globale
</dt> <dd>

**Annonces \_ type de groupe groupes \_ \_ globaux \_** \| **ad groupe annonces \_ \_ \_ sécurité \_ activée**

</dd> <dt>

<span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Distribution universelle
</dt> <dd>

**\_ \_ groupe universel de type groupe \_ ad \_**

</dd> <dt>

<span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Sécurité universelle
</dt> <dd>

**Annonces \_ \_type de \_ \_** groupe annonces de groupe universel sécurité de type de groupe \| **\_ \_ \_ \_ activée**

</dd> <dt>


</dt> <dd>

</dd> </dl>

Si le groupe est conçu pour définir le contrôle d’accès sur les objets d’annuaire, le groupe doit être un groupe de sécurité global ou universel.

Sachez que les groupes de sécurité universels ne peuvent être créés que sur des domaines Windows 2000 s’exécutant en mode natif. Pour plus d’informations sur la détection du mode mixte et le mode natif, consultez [détection du mode d’opération d’un domaine](detecting-the-operation-mode-of-a-domain.md).

</dd> <dt>

<span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**sAMAccountName**
</dt> <dd>

Contient une chaîne qui est le nom utilisé pour prendre en charge les clients et les serveurs d’une version précédente. Le **sAMAccountName** doit comporter moins de 20 caractères pour prendre en charge les clients d’une version précédente de Windows.

**SAMAccountName** doit être unique parmi tous les objets principaux de sécurité au sein du domaine. Une requête doit être exécutée sur le domaine pour vérifier que le **sAMAccountName** est unique au sein du domaine.

</dd> </dl>

Les membres du groupe peuvent être ajoutés au moment de la création à l’aide de la méthode [**IDirectoryObject :: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) . Si vous le souhaitez, des membres peuvent être ajoutés au groupe après la création à l’aide de la méthode [**IADsGroup :: Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) . Pour plus d’informations sur l’ajout de membres à un groupe, consultez [Ajout de membres à des groupes dans un domaine](adding-members-to-groups-in-a-domain.md).

 

 