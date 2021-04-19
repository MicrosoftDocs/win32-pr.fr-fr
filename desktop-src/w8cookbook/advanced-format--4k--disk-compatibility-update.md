---
title: Mise à jour de compatibilité des disques au format avancé (4K)
description: Mise à jour de compatibilité des disques au format avancé (4K)
ms.assetid: 2C9EB0CF-D27B-457A-8FE6-24824BCC084C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbad505575c4479bd750f09ccd83bc4da4c39667
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314972"
---
# <a name="advanced-format-4k-disk-compatibility-update"></a>Mise à jour de compatibilité des disques au format avancé (4K)

## <a name="platforms"></a>Plateformes

**Clients**   Windows XP, Windows Vista, Windows 7, Windows 7 SP1, Windows 8  
**Serveurs**   Windows Server 2003, Windows Server 2008, Windows Server 2008 R2, Windows Server 2008 R2 SP1, Windows Server 2012, Windows Server 2012 R2 et Windows Server 2016  


## <a name="description"></a>Description

Cet article est une version mise à jour de l’article intitulé mise à jour de compatibilité des disques émulation (émulation de l’octet 512) qui a été publiée pour Windows 7 SP1 et Windows Server 2008 R2 SP1. Cette mise à jour contient des informations très nouvelles, dont certaines s’appliquent uniquement à Windows 8 et Windows Server 2012.

Les densités de zone sont en augmentation annuelle et avec l’avènement récente de disques de 3 to, les mécanismes de correction d’erreur utilisés pour gérer le rapport de signal à bruit (SNR) diminuant la baisse de l’espace sont devenus inefficaces. autrement dit, une augmentation de la charge est nécessaire pour garantir que le média est utilisable. L’une des solutions de l’industrie du stockage pour améliorer ce mécanisme de correction des erreurs consiste à introduire un format de support physique différent qui comprend une plus grande taille de secteur physique. Ce nouveau format de média physique est appelé format avancé. Par conséquent, il n’est plus sûr de faire des hypothèses concernant la taille des secteurs des appareils de stockage modernes, et les développeurs doivent étudier les hypothèses sous-jacentes de leur code pour déterminer s’il y a un impact.

Cette rubrique présente l’effet des dispositifs de stockage de format avancés sur les logiciels, explique ce que les applications peuvent faire pour aider à prendre en charge ce type de média et présente l’infrastructure que Microsoft a introduite avec Windows Vista, Windows 7 et Windows 8 pour permettre aux développeurs de prendre en charge ces types d’appareils. Tandis que les éléments présentés dans cette rubrique fournissent des instructions pour améliorer la compatibilité avec les disques au format avancé, les informations s’appliquent généralement à tous les systèmes avec des disques au format avancé exécutant Windows Vista, Windows 7 et Windows 8.

**Résumé des nouvelles fonctionnalités liées aux grands secteurs**

La liste ci-dessous récapitule les nouvelles fonctionnalités fournies dans le cadre de Windows 8 et de Windows Server 2012 afin d’améliorer l’expérience des clients et des développeurs avec des disques de secteurs importants. Description plus détaillée de chaque élément.

-   S’appuie sur la prise en charge de Windows 7 SP1 pour les disques 4 Ko avec émulation (émulation) et fournit une prise en charge complète de la boîte de réception pour les disques avec une taille de secteur de 4 Ko sans émulation (4 Ko natifs). Voici quelques exemples d’applications et de scénarios pris en charge :
    -   Possibilité d’installer Windows to et de démarrer à partir d’un disque de secteur 4K sans émulation (disque natif 4K)
    -   VHD et nouveau format de fichier VHDX
    -   Prise en charge de HyperV complète
    -   Sauvegarde Windows
    -   Prise en charge complète dans le système de fichiers NT (NTFS)
    -   Prise en charge complète avec de nouveaux espaces de stockage et pools (SSP)
    -   Prise en charge complète avec Windows Defender
-   Fournit une nouvelle API pour interroger la taille de secteur physique (FileFsSectorSizeInformation) :
    -   Disponible pour les volumes réseau
    -   Peut être délivré à n’importe quel handle de fichier
    -   Disponible pour les applications non privilégiées
    -   Modèle d’utilisation plus convivial
-   Comprend l’utilitaire de ligne de commande fsutil amélioré pour interroger la taille de secteur logique et physique du volume avec les informations d’alignement (la version de base de l’utilitaire sans informations d’alignement est disponible pour Windows 7 avec Microsoft KB 982018 et Windows Server 2008 R2 avec Microsoft KB 982018)

**Présentation des disques au format avancé (4 Ko)**

L’un des problèmes liés à l’introduction de cette modification dans le format multimédia est la possibilité d’introduire des problèmes de compatibilité avec les logiciels et le matériel existants. En guise de solution de compatibilité temporaire, le secteur du stockage commence par introduire des disques qui émulent un disque de secteur standard de 512 octets, mais qui rendent disponibles des informations sur la taille réelle des secteurs via des commandes ATA et SCSI standard. À la suite de cette émulation, il existe, essentiellement, deux tailles de secteur :

**Secteur logique :** Unité utilisée pour l’adressage de bloc logique pour le média. Nous pouvons également considérer qu’il s’agit de la plus petite unité d’écriture que le stockage peut accepter. Il s’agit de l’émulation.   
**Secteur physique :** L’unité pour laquelle les opérations de lecture et d’écriture sont effectuées sur l’appareil en une seule opération. Il s’agit de l’unité d’écriture atomique.  
 La plupart des API Windows actuelles, telles \_ que \_ le disque IOCTL obtiennent \_ \_ une géométrie de lecteur, retournent la taille de secteur logique, mais la taille de secteur physique peut être récupérée par le biais du code de contrôle de propriété de <a href="/windows-hardware/drivers/ddi/content/ntddstor/ni-ntddstor-ioctl_storage_query_property"> \_ \_ requête \_ de stockage IOCTL</a> , avec les informations pertinentes contenues dans le champ BytesPerPhysicalSector de la structure du <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor"> \_ \_ \_ descripteur d’alignement de l’accès au stockage</a> . Ce sujet est abordé plus en détail plus loin dans cet article.

**Types initiaux des médias de grands secteurs**

Le secteur du stockage a rapidement mis en œuvre des efforts de transition vers ce nouveau type de stockage avancé pour les médias ayant une taille de secteur physique de 4 Ko. Deux types de médias seront publiés sur le marché :

**4 Ko natifs :** Ce support n’a pas de couche d’émulation et expose directement 4 Ko comme taille de secteur logique et physique. Le problème global de ce nouveau type de média est que la majorité des applications et des systèmes d’exploitation ne recherchent pas et alignent les e/s sur la taille de secteur physique, ce qui peut entraîner des e/s ayant échoué inattendues.  
**512-émulation d’octet (émulation) :** Ce support a une couche d’émulation comme indiqué dans la section précédente et expose 512-octets comme taille de secteur logique (semblable à un disque normal aujourd’hui), mais rend ses informations de taille de secteur physique (4 Ko) disponibles. Le problème global de ce nouveau type de média est que la majorité des applications et des systèmes d’exploitation ne comprennent pas l’existence de la taille de secteur physique, ce qui peut entraîner un certain nombre de problèmes, comme indiqué ci-dessous.  
**Prise en charge globale de Windows pour les grands secteurs**

Ce tableau décrit la politique officielle de support Microsoft pour les différents médias et leurs tailles de secteurs signalées. Pour plus d’informations, consultez cet article de la [base de connaissances](https://support.microsoft.com/kb/2510009) .



| Noms communs                                  | Taille de secteur logique signalée | Taille de secteur physique signalée | Version de Windows avec prise en charge                                                                                                                                                                                                                                                                             |
|-----------------------------------------------|------------------------------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 512 octets natif, 512N                         | 512 octets                    | 512 octets                     | Toutes les versions de Windows                                                                                                                                                                                                                                                                                     |
| Format avancé, émulation, AF, émulation de 512 octets | 512 octets                    | 4 Ko                          | Windows Vista avec MS KB 2553708 <br/> Windows Server 2008 \* avec MS ko 2553708 <br/> Windows 7 avec MS KB 982018 <br/> Windows Server 2008 R2 * avec MS KB 982018 <br/> Toutes les versions de Windows à partir de Windows 7 SP1 et versions ultérieures. <br/> Toutes les versions serveur du serveur 2008 R2 SP1 et versions ultérieures. <br/> <br/> \*Sauf pour Hyper-V. Consultez la section [« spécifications de prise en charge des applications pour les lecteurs de secteurs importants »](https://support.microsoft.com/help/2510009/microsoft-support-policy-for-4k-sector-hard-drives-in-windows) . |
| Advanced format, AF, 4K native, 4Kn            | 4 Ko                         | 4 Ko                          | Toutes les versions de Windows à partir de Windows 8 et versions ultérieures <br/> Toutes les versions serveur de Windows Server 2012 et versions ultérieures <br/>                                                                                                                                                                                                                                                      |
| Autres                                         | Pas 4 Ko ou 512 octets        | Pas 4 Ko ou 512 octets         | Non pris en charge                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> Bien qu’ils ne soient pas soulignés dans le tableau précédent, Windows XP, Windows Server 2003 et Windows Server 2003 R2 ne prennent pas en charge les supports émulation ou 4Kn. Si le système peut démarrer et être en mesure de fonctionner au minimum, il peut y avoir des scénarios inconnus de problèmes de fonctionnalité, de perte de données ou de performances non optimales. Par conséquent, Microsoft recommande vivement d’utiliser des médias émulation avec Windows XP ou d’autres produits basés sur le code base Windows XP (par exemple, Windows édition Windows Server 1,0, Windows Server 2003, Windows Server 2003 R2, Windows XP 64 bits, Windows XP Embedded, Windows Small Business Server 2003 et Windows Small Business Server 2003 R2).

 

## <a name="how-emulation-works-read-modify-write-rmw"></a>Fonctionnement de l’émulation : lecture-modification-écriture (RMW)

Un support de stockage a une certaine unité dans laquelle le support physique peut être modifié. Autrement dit, le support peut uniquement être écrit, ou réécrit, dans des unités de la taille de secteur physique. Par conséquent, les écritures qui ne sont pas exécutées à ce niveau d’unité nécessitent des étapes supplémentaires, que nous allons examiner dans l’exemple ci-dessous.

Dans ce scénario, une application doit mettre à jour le contenu d’un enregistrement DataStor situé dans un secteur logique de 512 octets. Ce diagramme illustre les étapes nécessaires pour que le périphérique de stockage termine l’écriture :

![étapes pour qu’un dispositif de stockage termine une écriture](images/512ermwsteps.png)

Comme illustré ci-dessus, ce processus implique un travail du dispositif de stockage qui peut entraîner une perte de performances. Pour éviter ce travail supplémentaire, les applications doivent être mises à jour pour :

-   Requête pour la taille de secteur physique
-   Vérifier que les écritures sont alignées sur la taille de secteur physique indiquée

Bien que cela puisse paraître initialement être un problème de performance, il peut y avoir un problème plus sérieux. Passons à ce sujet dans la section suivante.

**Résilience : coût masqué de lecture-modification-écriture**

La résilience est la capacité d’une application à récupérer l’état entre les sessions. Nous avons vu ce qui est nécessaire pour qu’un dispositif de stockage émulation exécute un secteur de 512 octets pour écrire le cycle de lecture-modification-écriture. Observons ce qui se passe si le processus de remplacement du secteur physique précédent sur le support a été interrompu. Quelles sont les conséquences ?

-   Étant donné que la plupart des lecteurs de disque dur sont mis à jour en place, le secteur physique qui est, la partie du support où se trouvait le secteur physique pourrait avoir été endommagé avec des informations incomplètes en raison d’un remplacement partiel. En d’autres termes, vous pouvez le considérer comme susceptible d’avoir perdu les 8 secteurs logiques que le secteur physique contient logiquement.
-   Alors que la plupart des applications avec un magasin de données sont conçues avec la possibilité de récupérer à partir d’erreurs de support, la perte de huit secteurs ou d’une autre façon, la perte de huit enregistrements de validation, peut potentiellement empêcher la récupération normale de la Banque de données. Un administrateur peut avoir besoin de restaurer manuellement la base de données à partir d’une sauvegarde ou de devoir effectuer une reconstruction longue.
-   Un impact plus important est que l’acte d’une autre application provoquant un cycle de lecture-modification-écriture peut potentiellement entraîner la perte de vos données même si votre application n’est pas en cours d’exécution ! Cela est tout simplement dû au fait que vos données et les autres données de l’application peuvent se trouver dans le même secteur physique.

Dans ce cas, il est important que les logiciels d’application réévaluent les hypothèses prises dans le code, et qu’ils soient conscients de la différence de taille de secteur physique logique, ainsi que certains scénarios clients intéressants décrits plus loin dans cet article.

**Faire la bonne chose (éviter les opérations de lecture-modification-écriture)**

Si certains fournisseurs de stockage peuvent introduire des niveaux d’atténuation au sein de certains dispositifs de stockage émulation pour tenter de faciliter les problèmes de performances et de résilience du cycle de lecture-modification-écriture, il n’y a que peu d’atténuation pouvant être gérée en termes de charge de travail. Par conséquent, les applications ne doivent pas s’appuyer sur cette atténuation comme une solution à long terme. De plus, il n’y a aucune garantie que toutes les classes de disques auront cette atténuation en place, et qu’il n’y a pas de garantie que l’atténuation est bien conçue.

La solution à cela n’est pas une atténuation dans le lecteur, mais pour concevoir des applications qui font le bon ensemble de choses pour aider à prendre en charge ce type de média. Cette section décrit les scénarios courants dans lesquels les applications peuvent rencontrer des problèmes avec les disques de secteurs importants et suggère un moyen d’investigation pour essayer et résoudre chaque problème.

**Problème 1 : la partition n’est pas alignée sur une limite de secteur physique**

Lorsque l’administrateur/l’utilisateur partitionne le disque, la première partition n’a peut-être pas été créée sur une limite alignée. Cela peut entraîner la non-alignement de toutes les écritures suivantes sur les limites du secteur physique. À compter de Windows Vista SP1 et de Windows Server 2008, la première partition est placée au premier 1024 Ko du disque (pour les disques 4 Go ou plus, sinon l’alignement est de 64 Ko) qui est aligné sur une limite de secteur physique de 4 Ko. Toutefois, étant donné le partitionnement par défaut dans Windows XP, un utilitaire de partitionnement tiers ou une utilisation incorrecte des API Windows, les partitions créées peuvent ne pas être alignées sur une limite de secteur physique. Les développeurs doivent s’assurer que les API correctes sont utilisées pour garantir l’alignement. Les API recommandées pour garantir l’alignement des partitions sont décrites ci-dessous.

Les API IVdsPack :: CreateVolume et IVdsPack2 :: CreateVolume2 n’utilisent pas le paramètre d’alignement spécifié lors de la création d’un nouveau volume, mais utilisent plutôt la valeur d’alignement par défaut pour le système d’exploitation (pré-Windows Vista SP1 utilise 63 octets, et Windows Vista SP1 utilise les valeurs par défaut indiquées ci-dessus). Utilisez plutôt les API IVdsCreatePartitionEx :: CreatePartitionEx ou IVdsAdvancedDisk :: CreatePartition qui utilisent le paramètre d’alignement spécifié pour les applications qui doivent créer des partitions.

La meilleure façon de s’assurer que l’alignement est correct est de le faire juste lors de la création initiale de la partition. Dans le cas contraire, votre application devra prendre en compte l’alignement lors de l’exécution d’écritures ou de l’initialisation, ce qui peut être un processus très complexe.

**Problème 2 : écritures non mises en mémoire tampon non alignées sur la taille de secteur physique**

Le problème le plus simple est que les écritures non mises en mémoire tampon ne sont pas alignées sur la taille de secteur physique indiquée du support de stockage. Les écritures mises en mémoire tampon, en revanche, sont alignées sur la taille de page de 4 Ko, ce qui est par conséquent la taille de secteur physique de la première génération de médias de grands secteurs. Toutefois, la plupart des applications avec un magasin de données effectuent des écritures non mises en mémoire tampon et doivent donc s’assurer que ces écritures sont effectuées dans des unités de la taille de secteur physique.

Voici quelques exemples de scénarios dans lesquels l’e/s d’application obtenue n’est pas alignée :

**Les enregistrements de validation sont remplis à des secteurs de 512 octets :** Les applications avec un magasin de données ont généralement une forme d’enregistrement de validation qui conserve des informations sur les modifications des métadonnées ou gère la structure de la Banque de données. Pour éviter que la perte d’un secteur n’affecte plusieurs enregistrements, cet enregistrement de validation est généralement rempli à une taille de secteur. Avec un disque avec une plus grande taille de secteur physique, l’application doit interroger la taille de secteur physique comme indiqué dans la section précédente et vérifier que chaque enregistrement de validation est rempli à cette taille. Avec un disque de 4 Ko, cela garantit que les e/s n’échouent pas. Avec un disque émulation, non seulement vous évitez le cycle de lecture-modification-écriture, mais cela permet de garantir que, en cas de perte d’un secteur physique, un seul enregistrement de validation serait perdu.  
**Les fichiers journaux sont écrits dans des blocs non alignés :** Les e/s non mises en mémoire tampon sont généralement utilisées lors de la mise à jour ou de l’ajout d’un fichier journal. Les applications peuvent basculer vers des e/s mises en mémoire tampon ou mettre en mémoire tampon les mises à jour des journaux vers des unités de la taille de secteur physique pour éviter les e/s qui ont échoué ou déclencher une lecture-modification-écriture.  
 Pour vous aider à déterminer si votre application émet des e/s non mises en mémoire tampon, veillez à inclure l' \_ \_ indicateur de fichier sans indicateur \_ de mise en mémoire tampon dans le paramètre *dwFlagsAndAttributes* lorsque vous appelez la fonction CreateFile.

En outre, si vous alignez actuellement les écritures sur la taille de secteur, cette taille de secteur est très probablement la taille de secteur logique, car la plupart des API existantes qui interrogent la taille de secteur des supports interrogent simplement l’unité d’adressage, c’est-à-dire la taille de secteur logique. La taille de secteur d’intérêt ici est la taille de secteur physique, qui est l’unité réelle d’atomicité. Voici quelques exemples d’API qui récupèrent la taille de secteur logique :

-   GetDiskFreeSpace, GetDiskFreeSpaceEx
-   FileFsVolumeInformation
-   \_disque IOCTL \_ obtient la géométrie du \_ lecteur \_ , IOCTL \_ Disk \_ obtient la géométrie du \_ lecteur \_ \_ ex
-   IVdsDisk :: GetProperties, IVdsDisk3 :: GetProperties2

Voici comment vous pouvez interroger la taille de secteur physique :

**Méthode recommandée pour Windows 8**

Avec Windows 8, Microsoft a introduit une nouvelle API qui permet aux développeurs d’intégrer facilement la prise en charge 4K dans leurs applications. Cette nouvelle API prend en charge un nombre de scénarios encore plus élevé que la méthode héritée pour Windows Vista et Windows 7, comme indiqué ci-dessous. Cette API active ces scénarios d’appel :

-   Appel à partir d’une application non privilégiée
-   Appel à un handle de fichier valide
-   Appel à un descripteur de fichier sur un volume distant sur SMB2
-   Modèle de programmation simplifié

L’API se présente sous la forme d’une nouvelle classe d’informations, FileFsSectorSizeInformation, avec les informations de taille de secteur FS de fichier de structure associées \_ \_ \_ \_ , définies comme suit :


```
typedef struct _FILE_FS_SECTOR_SIZE_INFORMATION {  
    ULONG LogicalBytesPerSector;  
    ULONG PhysicalBytesPerSectorForAtomicity;  
    ULONG PhysicalBytesPerSectorForPerformance;  
    ULONG FileSystemEffectivePhysicalBytesPerSectorForAtomicity;  
    ULONG Flags;  
    ULONG ByteOffsetForSectorAlignment;  
    ULONG ByteOffsetForPartitionAlignment;  
} FILE_FS_SECTOR_SIZE_INFORMATION, *PFILE_FS_SECTOR_SIZE_INFORMATION;
```



**Méthode héritée pour Windows 7 et Windows Vista**

Windows Vista et Windows Server 2008 ont introduit des API pour interroger la taille de secteur physique de l’unité de stockage connectée pour les contrôleurs de stockage basés sur AHCI. Avec Windows 7 et Windows Server 2008 R2, à compter de SP1 (ou de la base de connaissances Microsoft 982018), cette prise en charge est étendue aux contrôleurs de stockage basés sur Storport. Microsoft a fourni un [exemple de code](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor) sur MSDN détaillant comment une application peut interroger la taille de secteur physique du volume.

Bien que l’exemple de code ci-dessus vous permette d’obtenir la taille de secteur physique du volume, vous devez effectuer un contrôle d’intégrité de base de la taille de secteur physique indiquée avant de l’utiliser, car il a été observé que certains pilotes ne retournent pas de données correctement mises en forme :

-   Assurez-vous que la taille de secteur physique indiquée est >= la taille de secteur logique signalée ; Si ce n’est pas le cas, votre application doit utiliser une taille de secteur physique égale à la taille de secteur logique signalée
-   Assurez-vous que la taille de secteur physique indiquée est une puissance de deux ; Si ce n’est pas le cas, votre application doit utiliser une taille de secteur physique égale à la taille de secteur logique signalée
-   Si la taille de secteur physique est une valeur Power-of-Two comprise entre 512 octets et 4 Ko, vous devez envisager d’utiliser une taille de secteur physique arrondie à la taille de secteur logique signalée.
-   Si la taille de secteur physique est une valeur Power-of-Two supérieure à 4 Ko, vous devez évaluer la capacité de votre application à gérer ce scénario avant d’utiliser cette valeur. dans le cas contraire, vous devez envisager d’utiliser une taille de secteur physique arrondie à 4 Ko.

L’utilisation de cette IOCTL pour obtenir la taille de secteur physique présente plusieurs limitations. Elle effectue les actions suivantes :

-   Requiert un privilège élevé ; Si votre application ne s’exécute pas avec le privilège, vous devrez peut-être écrire une application de service Windows comme indiqué ci-dessus
-   Ne prend pas en charge les volumes SMB ; vous devrez peut-être également écrire une application de service Windows pour prendre en charge l’interrogation de la taille des secteurs physiques sur ces volumes
-   Ne peut pas être émis pour un handle de fichier (l’IOCTL doit être délivré à un handle de volume)

**Problème 3 : formats de fichiers basés sur des secteurs de 512 octets**

Certaines applications avec des formats de fichier standard (tels que VHD 1,0) peuvent avoir des fichiers codés en dur pour supposer une taille de secteur de 512 octets. Ainsi, les mises à jour et les écritures dans ce fichier entraîneraient un cycle de lecture-modification-écriture sur l’appareil, ce qui entraînera potentiellement des problèmes de performances et de résilience pour vos clients. Toutefois, il existe des moyens pour une application de prendre en charge l’utilisation de ce type de média, par exemple :

-   Utilisez la mise en mémoire tampon pour vous assurer que les écritures sont effectuées dans les unités de la taille de secteur physique
-   Implémentez une lecture-modification-écriture interne qui peut aider à garantir que les mises à jour sont effectuées dans les unités de la taille de secteur physique indiquée.
-   Si possible, compléter les enregistrements dans un secteur physique, de telle sorte que le remplissage soit interprété comme un espace vide
-   Envisagez de reconcevoir une version de la structure de données de l’application avec prise en charge des secteurs plus grands

**Problème 4 : la taille de secteur physique signalée peut changer d’une session à l’autre**

Il existe de nombreux scénarios dans lesquels la taille de secteur physique signalée du stockage sous-jacent qui héberge le DataStor peut changer. Le plus souvent, c’est lorsque vous migrez le DataStor vers un autre volume, ou même sur le réseau. Une modification de la taille de secteur physique signalée peut être un événement inattendu pour de nombreuses applications et peut entraîner l’échec de la réinitialisation de certaines applications.

Il ne s’agit pas du scénario le plus simple pour prendre en charge et est mentionné ici comme un avis. Vous devez prendre en compte les besoins de mobilité de vos clients et ajuster votre support en conséquence pour vous assurer que les clients ne sont pas affectés négativement à l’aide d’un média émulation ou natif 4K.

**Comment un utilisateur peut récupérer la taille de secteur logique et physique pour un volume**

L’utilitaire with Windows est un utilitaire permettant d’afficher les informations de taille de secteur pour un volume. Les versions de Windows avec fsutil pris en charge sont les suivantes :

-   Windows 8
-   Windows Server 2012
-   Windows 7 SP1 avec Microsoft KB 982018
-   Windows 7 avec Microsoft KB 982018
-   Windows Server 2008 R2 SP1 avec Microsoft KB 982018 (v3)
-   Windows Server 2008 R2 avec Microsoft KB 982018 (v3)
-   Windows Vista avec Microsoft KB 2553708
-   Windows Server 2008 avec Microsoft KB 2553708

Pour afficher les informations sur la taille des secteurs, appelez l’utilitaire comme suit à partir d’une invite de commandes avec élévation de privilèges :


```
fsutil fsinfo ntfsinfo <drive letter>
```



Un disque de secteur 4K avec émulation de 512 octets a le champ octets par secteur défini sur 512 et le champ octets par secteur physique défini sur 4096 comme suit :

![octets par secteur et par secteur physique d’un disque de secteur 4k avec émulation de 512 octets](images/4ksectordiskwith512emulation.png)

Un disque natif de 4 Ko contient le nombre d’octets par secteur et d’octets par champ de secteur physique définis sur 4096 comme suit :

![octets par secteur et par secteur physique d’un disque natif de 4 Ko](images/4knativedisk.png)

> [!Note]  
> Si le champ octet par secteur physique affiche non pris en charge, soit le pilote de stockage ne prend pas en charge la \_ \_ propriété de requête de stockage IOCTL, soit \_ une erreur s’est produite lors de la récupération des informations.

 

## <a name="resources"></a>Ressources

-   [Déclaration de support général Windows](https://support.microsoft.com/kb/2510009)
-   [Microsoft KB 982018](https://support.microsoft.com/kb/982018)
-   [Microsoft KB 2553708](https://support.microsoft.com/kb/2553708)
-   [Correctif logiciel pour Windows 7 et Windows Server 2008 R2](https://support.microsoft.com/kb/982018)
-   [Correctif logiciel pour Windows Vista et Windows Server 2008](https://support.microsoft.com/kb/2553708)
-   [HyperV (instruction de prise en charge)](https://support.microsoft.com/kb/2515143)
-   [Informations générales sur le code de contrôle de la propriété de requête de \_ stockage IOCTL \_ \_](/windows-hardware/drivers/ddi/ntddstor/ni-ntddstor-ioctl_storage_query_property)
-   [\_Code de \_ contrôle de propriété de requête de stockage IOCTL \_](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property)
-   [Informations générales sur la \_ structure du \_ descripteur d’alignement de l’accès au stockage \_](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-_storage_access_alignment_descriptor)
-   [Description de la terminologie standard utilisée pour décrire les mises à jour logicielles Microsoft](https://support.microsoft.com/kb/824684/)
-   [Exemple de code WDK avec des détails sur la façon d’extraire les informations d’alignement d’accès de stockage signalées à partir de la \_ structure du descripteur d’alignement de l’accès au stockage \_ lors d' \_ un appel au \_ Code de contrôle de propriété de requête de stockage IOCTL \_ \_](/windows/win32/api/winioctl/ns-winioctl-storage_access_alignment_descriptor)
-   [Informations générales sur les options d’ImageX Command-Line](/previous-versions/windows/it-pro/windows-7/dd799302(v=ws.10))
-   [Pilotes de chipset Intel requis pour prendre en charge les lecteurs de secteur de 4 Ko](https://www.intel.com/support/chipsets/imsm/sb/CS-031502.htm)

 

