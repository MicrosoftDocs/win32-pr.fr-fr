---
title: Création d’une partition d’annuaire d’applications
description: Une partition de l’annuaire d’applications est représentée par un objet domainDNS avec une valeur d’attribut instanceType de DS \_ instanceType \_ . l' \_ \_ en-tête NC instanceType est accessible en \_ \_ \_ \_ écriture.
ms.assetid: 5e90f316-9d67-484d-98b8-0632dd3c2c43
ms.tgt_platform: multiple
keywords:
- Création d’une partition d’annuaire d’applications AD
- Partitions de l’annuaire d’applications Active Directory, création
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c340bac215be62867dcddcda97326c33fc70c458ee242965258cc1ee24cf25f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118020538"
---
# <a name="creating-an-application-directory-partition"></a>Création d’une partition d’annuaire d’applications

Une partition de l’annuaire d’applications est représentée par un objet [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) avec une valeur d’attribut [**instanceType**](/windows/desktop/ADSchema/a-instancetype) de **DS instanceType. l' \_ \_ \_ \_ en-tête NC** instanceType est **accessible en \_ \_ \_ \_ écriture**. Cet objet **domainDNS** représente la racine de la partition de l’annuaire d’applications (en-tête du NC) et est nommé comme une partition de domaine normale, par exemple « DC = DYNAMICDATA, DC = fabrikam, DC = com », qui correspond à un nom DNS « DynamicData.fabrikam.com ». Une partition d’annuaire d’applications peut, par conséquent, être instanciée partout où une partition de domaine peut être instanciée. Aucun nom NetBIOS n’est associé à une partition d’annuaire d’applications.

Il est possible d’imbriquer des partitions d’annuaire d’applications, autrement dit, une partition d’annuaire d’applications peut avoir des partitions d’annuaire d’applications enfants. Les recherches avec une étendue de sous-arborescence associée à une racine de la partition de l’annuaire d’applications génèrent des références de continuation aux partitions de l’annuaire d’applications enfant.

un réplica de partition d’annuaire d’applications ne peut être créé que sur un contrôleur de domaine qui s’exécute sur Windows server 2003 et versions ultérieures, et uniquement si le rôle FSMO Domain-Naming est détenu par un contrôleur de domaine Windows Server 2003 et ultérieur. dans une forêt mixte qui a à la fois des contrôleurs de domaine Windows Server 2003 et des contrôleurs de domaine de niveau supérieur (Windows des contrôleurs de domaine 2000 ou des contrôleurs de domaine principaux Windows NT 4,0), une tentative de création d’un réplica de partition d’annuaire d’application sur un contrôleur de domaine de niveau supérieur échouera.

Une partition d’annuaire d’applications a également un objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) correspondant dans le conteneur partitions de la partition de configuration. Le **crossRef** peut être créé au préalable manuellement avant la création de l’objet [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) . L’objet **crossRef** créé au préalable doit avoir les valeurs d’attribut indiquées dans le tableau suivant, sinon la création de la partition échouera. Si l’objet **crossRef** n’existe pas, le serveur Active Directory en crée un lors de la création de la partition d’annuaire d’applications.

| Attribut                          | Description                                                                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) | Contient le chemin d’accès DNS du contrôleur de domaine sur lequel la partition d’annuaire d’applications sera créée.                               |
| [**Activé**](/windows/desktop/ADSchema/a-enabled) | Contient la **valeur false**.                                                                                                                       |
| [**nCName**](/windows/desktop/ADSchema/a-ncname)   | Contient le nom unique de la partition. Dans l’exemple ci-dessus, cet attribut contiendra « DC = DynamicData, DC = MyDomain, DC = com ». |



 

**Pour créer une nouvelle partition d’annuaire d’applications avec son premier réplica, procédez comme suit :**

1.  Connectez-vous à l’espace de noms pour la nouvelle partition, en spécifiant le contrôleur de domaine qui hébergera la partition de l’annuaire d’applications dans l’ADsPath. Par exemple, pour créer une partition avec un ADsPath de « DC = DynamicData, DC = MonDomaine, DC = com », la liaison ADsPath est « LDAP:// <domain controller> /DC = MyDomain, DC = com », où « &lt; contrôleur de domaine &gt; » est le nom DNS du contrôleur de domaine qui hébergera la partition.

    L’opération de liaison doit spécifier les options Fast et delegation. L’option fast permet à la liaison de se dérouler même si l’espace de noms n’existe pas. L’option de délégation est requise pour permettre au contrôleur de domaine de contacter le détenteur du rôle Domain-Naming FSMO en utilisant les mêmes informations d’identification.

    la version système du contrôleur de domaine doit être Windows système d’exploitation Server 2003 et versions ultérieures.

2.  Créez un objet [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) avec un nom approprié pour la partition, par exemple, « DC = DynamicData » pour représenter l’en-tête de contexte d’appellation pour la nouvelle partition. L’objet **domainDNS** doit avoir un attribut [**instanceType**](/windows/desktop/ADSchema/a-instancetype) avec une valeur de 5 (le **DS \_ instanceType est le NC \_ \_ \_** \| **\_ instanceType \_ NC instanceType NC \_ est accessible en \_ écriture**). L’attribut **instanceType** ne peut être défini qu’au moment de la création, car il s’agit d’un attribut système uniquement.

Lorsque l’objet [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) est créé, le serveur Active Directory effectue les étapes suivantes :

1.  Recherche un objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) dans le conteneur partitions qui a une valeur d’attribut [**NCName**](/windows/desktop/ADSchema/a-ncname) qui correspond au nom unique de la partition et, si une correspondance est trouvée, modifie l’objet **crossRef** pour représenter la partition d’annuaire d’applications. Si aucun objet **crossRef** correspondant n’est trouvé, le serveur Active Directory crée un nouvel objet **crossRef** pour représenter la partition de l’annuaire d’applications.

    Le tableau suivant répertorie les attributs importants de l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) .

    | Attribut                                                              | Description                                                                                                                                        |
    |------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**nCName**](/windows/desktop/ADSchema/a-ncname)                                       | Contient le nom unique de la partition.                                                                                                  |
    | [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot)                                     | Contient le nom DNS de la partition.                                                                                                            |
    | [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) | Le nom unique de l’objet [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) du contrôleur de domaine pour le premier réplica est ajouté à cet attribut. |

    

     

2.  Lancez une synchronisation de la partition de configuration et attendez la fin de l’opération. Cela permet à l’application cliente de modifier les paramètres de configuration de la nouvelle partition d’annuaire d’applications, tout en étant lié au même contrôleur de domaine utilisé pour la création de la partition d’annuaire d’applications.
3.  La création de l’objet [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) avec le **DS \_ instanceType \_ est l' \_ \_ en-tête NC** et le contrôleur de **service Active Directory \_ instanceType est un indicateur accessible en \_ \_ \_ écriture** défini sur la propriété [**INSTANCETYPE**](/windows/desktop/ADSchema/a-instancetype) . La propriété **instanceType** peut également contenir d’autres indicateurs privés.
4.  Remplissez l’attribut [**ms-DS-has-Master-NC**](/windows/desktop/ADSchema/a-msds-hasmasterncs) de l’objet [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) du contrôleur de domaine cible avec le nom unique de la partition d’annuaire d’applications nouvellement créée.

Lorsque la partition de l’annuaire d’applications est créée, ou lorsqu’un nouveau réplica de la partition de l’annuaire d’applications est ajouté et entièrement synchronisé, le serveur Active Directory inscrit correctement le réplica auprès du service Netlogon et DNS. Pour plus d’informations et pour obtenir la liste des enregistrements SRV inscrits, consultez [localisation d’un serveur hôte de partition d’annuaire d’applications](locating-an-application-directory-partition-host-server.md).

Pour plus d’informations sur la création d’une partition d’annuaire d’applications, consultez l' [exemple de code pour la création d’une partition d’annuaire d’applications](example-code-for-creating-an-application-directory-partition.md).

## <a name="locating-the-partitions-container"></a>Recherche du conteneur partitions

Le nom unique du conteneur de partitions peut être trouvé de deux manières. La première est plus compliquée à effectuer, mais elle fournira toujours un résultat précis :

1.  Liez à RootDSE et obtenez l’attribut **configurationNamingContext** .
2.  Utilisez l’attribut **configurationNamingContext** pour effectuer une liaison au conteneur de configuration.
3.  Recherchez dans le conteneur de configuration un objet de type [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) .
4.  Obtenez la valeur d’attribut **distinguishedName** de l’objet [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) . Il s’agit du nom unique du conteneur de partitions.

Pour plus d’informations et pour obtenir un exemple de code illustrant cette méthode pour localiser le conteneur partitions, consultez la fonction **GetPartitionsDNSearch** dans l' [exemple de code pour localiser le conteneur partitions](example-code-for-locating-the-partitions-container.md).

La deuxième méthode est plus facile à implémenter, mais elle s’appuie sur le conteneur partitions avec un nom unique relatif particulier. Il n’est pas possible actuellement de modifier le nom du conteneur partitions, mais si cette fonctionnalité est ajoutée à l’avenir, la procédure ci-dessous ne fonctionnera pas correctement si le conteneur partitions a été renommé.

1.  Liez à RootDSE et obtenez l’attribut **configurationNamingContext** .
2.  Combinez la chaîne « CN = Partitions » suivie de l’attribut **configurationNamingContext** pour former le nom unique du conteneur de partitions. Le nom unique se présente sous la forme « CN = Partitions <configuration DN> ».

Pour plus d’informations et pour obtenir un exemple de code illustrant cette méthode pour localiser le conteneur partitions, consultez la fonction **GetPartitionsDNManual** dans l' [exemple de code pour localiser le conteneur partitions](example-code-for-locating-the-partitions-container.md).

 

 