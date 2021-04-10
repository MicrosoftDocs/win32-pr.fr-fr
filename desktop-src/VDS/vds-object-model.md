---
description: Modèle d’objet VDS
ms.assetid: e5fcc19a-e170-4918-85eb-c1457776795a
title: Modèle d’objet VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae998955c5d0b7834cf4d88b901537f3644a2ab
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104211150"
---
# <a name="vds-object-model"></a>Modèle d’objet VDS

\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

VDS fournit un accès indirect aux dispositifs de stockage basés sur l’hôte, tels que les disques et les lecteurs de CD-ROM, et aux baies de disques qui sont gérées par les contrôleurs RAID matériels. Tandis que certaines entités de stockage modélisent des appareils physiques, d’autres modélisent des constructions virtuelles : des volumes, des partitions, etc. Les objets qui sont décrits dans cette rubrique représentent les entités physiques et virtuelles de VDS.

Les applications appellent les méthodes exposées par ces objets et VDS appellent le fournisseur approprié pour effectuer les opérations de stockage demandées. Une application n’appelle jamais directement un programme fournisseur.

### <a name="classification-of-objects"></a>Classification des objets

Comme le montre l’illustration suivante, les programmes de fournisseur de logiciels implémentent des objets qui modélisent des entités basées sur l’hôte. les programmes de fournisseur de matériel implémentent des objets qui modélisent des appareils RAID matériels internes et externes. les objets communs restants sont indépendants du fournisseur ou mis en œuvre par VDS. Une broche, qui n’est pas un objet VDS, est un terme de support de stockage générique qui se compose d’étendues de disque ou de lecteur.

![Diagramme qui montre une classification d’objets, définie comme « objets communs », « objets de fournisseur de logiciels » et « objets de fournisseur de matériel ».](images/vdsobjectmodel.png)

Pour en savoir plus sur le comportement de chaque objet, sélectionnez l’une des rubriques suivantes :

-   Le chargeur de service et les objets de service, consultez [démarrage et objets de service](startup-and-service-objects.md).
-   Les objets d’énumération et Async, consultez la page [objets d’assistance](helper-objects.md).
-   Fournisseur, consultez l' [objet Provider](provider-object.md).
-   Les objets Pack, disque, volume et Plex volume, consultez [objets fournisseur de logiciels](software-provider-objects.md).
-   Les objets de sous-système, de contrôleur, de lecteur, de LUN et de plex LUN, consultez la rubrique [objets de fournisseur de matériel](hardware-provider-objects.md).

### <a name="object-creation"></a>Création d’objets

Les opérations de configuration et de requête associées à la création d’objets peuvent prendre beaucoup de temps. par conséquent, VDS appelle toutes les méthodes de manière asynchrone. Le fournisseur de découverte retourne tous les événements de modification d’État, d’erreur ou d’achèvement. Les fournisseurs de logiciels journalisent également toutes les erreurs et les modifications d’État importantes.

### <a name="object-deletion"></a>Suppression de l'objet

Plusieurs méthodes VDS suppriment ou transforment des objets VDS. Un appelant peut conserver une référence, au moyen d’un pointeur d’interface, à un objet supprimé après le retour de la méthode. Lorsque l’appelant libère l’interface, VDS supprime l’objet.

En ce qui concerne la suppression d’objets, les appelants doivent s’abstenir d’appeler tout, à l’exception de la méthode [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur ces interfaces. Le fournisseur doit être suffisamment robuste pour traiter les appelants errants ; Si un appelant appelle une méthode sur un objet supprimé, le fournisseur doit retourner l' **\_ objet VDS \_ E \_ Deleted**.

### <a name="service-initialization"></a>Initialisation du service

VDS fournit un identificateur de classe (CLSID) pour le chargeur de service et les objets de service, mais seul le CLSID du chargeur de service est public. L’initialisation du service se produit lorsque les fournisseurs, une application appelante et le service effectuent les tâches suivantes :

-   Chaque nouveau fournisseur appelle la méthode [**IVdsAdmin :: RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) au cours de l’installation pour s’inscrire auprès de VDS. L’appel crée une clé de Registre sous la ruche système, identifiée par le GUID d’objet du fournisseur. Contenu sous cette clé est le CLSID de l’objet fournisseur, le nom, la version et le GUID de la version du fournisseur.
    > [!Note]  
    > Les GUID d’objet de fournisseur sont persistants ; les GUID d’objet logiciels et matériels ne le sont pas.

     

-   Une application appelle la fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , en passant le CLSID du chargeur de service comme argument. Avec un pointeur vers l’objet service Loader, l’application peut démarrer VDS localement ou à distance en transmettant le nom d’ordinateur souhaité en tant que paramètre à la méthode [**IVdsServiceLoader :: LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) .
-   Lorsque l’application initiale est attachée au service, VDS appelle d’abord [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) sur chaque CLSID trouvé sous la clé de Registre, puis appelle la méthode [**IVdsProviderPrivate :: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) sur chaque fournisseur pour initialiser les programmes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de VDS](about-vds.md)
</dt> <dt>

[**IVdsAdmin :: RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider)
</dt> <dt>

[**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[**IVdsProviderPrivate :: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> </dl>

 

 
