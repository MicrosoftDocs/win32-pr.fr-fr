---
description: Cette rubrique présente l’effet des dispositifs de stockage de format avancés sur les logiciels, explique ce que les applications peuvent faire pour aider à prendre en charge ce type de média et présente l’infrastructure que Microsoft a introduite avec Windows 7 SP1 et Windows Server 2008 R2 SP1 pour permettre aux développeurs de prendre en charge ces types d’appareils.
ms.assetid: 1D2847A7-15E9-42E0-90EB-7F43E76D3E44
title: Mise à jour de la compatibilité des disques Émulation 512 octets (512e)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94fbdce2937e2d121d892d8566755dfcb7f20f01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042803"
---
# <a name="512-byte-emulation-512e-disk-compatibility-update"></a>Mise à jour de la compatibilité des disques Émulation 512 octets (512e)

## <a name="platform"></a>Plateforme

 **Clients** -Windows Vista Windows 7 Windows 7 \| \| SP1  
**Serveurs** -windows Server 2008 \| Windows Server 2008 r2 \| Windows Server 2008 R2 SP1  

## <a name="feature-impact"></a>Impact sur les fonctionnalités

**Gravité** -haute  
**Fréquence** -élevée  









## <a name="description"></a>Description

Les densités de zone sont de plus en plus annuelles et, avec l’avènement récente de disques de 3 to, les mécanismes de correction d’erreur utilisés pour gérer le quotient de signal à bruit (SNR) diminuent l’efficacité de l’espace, c’est-à-dire qu’une quantité accrue de surcharge est nécessaire pour s’assurer que le média est utilisable. L’une des solutions de l’industrie du stockage pour améliorer ce mécanisme de correction des erreurs consiste à introduire un format de support physique différent qui comprend une plus grande taille de secteur physique. Ce nouveau format de média physique est appelé *format avancé*. Par conséquent, il n’est plus sûr de faire des hypothèses concernant la taille des secteurs des appareils de stockage modernes, et les développeurs doivent étudier les hypothèses sous-jacentes de leur code pour déterminer s’il y a un impact.

Cette rubrique présente l’effet des dispositifs de stockage de format avancés sur les logiciels, explique ce que les applications peuvent faire pour aider à prendre en charge ce type de média et discute de l’infrastructure pour permettre aux développeurs de prendre en charge ces types d’appareils. Bien que les éléments présentés dans cette rubrique fournissent des instructions pour améliorer la compatibilité avec les disques au format avancé, les informations s’appliquent généralement à tous les systèmes avec des disques au format avancé. Les versions suivantes de Windows assurent la prise en charge de l’interrogation de la taille des secteurs physiques :

-   Windows 7 avec Microsoft KB 982018
-   Windows 7 SP1
-   Windows Server 2008 R2 avec Microsoft KB 982018
-   Windows Server 2008 R2 SP1
-   Windows Vista avec Microsoft KB 2553708
-   Windows Server 2008 avec Microsoft KB 2553708

Pour plus d’informations, consultez [informations sur la politique de support Microsoft pour les lecteurs à grands secteurs dans Windows](https://support.microsoft.com/kb/2510009).

Pour plus d’informations sur les disques au format avancé, contactez votre fournisseur de stockage.

## <a name="logical-vs-physical-sector-size"></a>Taille logique et taille de secteur physique

L’un des problèmes liés à l’introduction de cette modification dans le format multimédia est la compatibilité avec les logiciels et matériels actuellement disponibles sur le marché dès aujourd’hui. En guise de solution temporaire, le secteur du stockage est à l’origine d’introduire des disques qui émulent un disque de secteur standard de 512 octets, mais qui rendent disponibles des informations sur la taille réelle des secteurs via des commandes ATA et SCSI standard. À la suite de cette émulation, il existe deux tailles de secteur :

-   **Secteur logique**: unité utilisée pour l’adressage de bloc logique pour le média. Nous pouvons également considérer qu’il s’agit de la plus petite unité d’écriture que le stockage peut accepter. Il s’agit de l’émulation.

-   **Secteur physique**: l’unité pour laquelle les opérations de lecture et d’écriture sur l’appareil sont effectuées en une seule opération. Il s’agit de l’unité d’écriture atomique.

La plupart des API Windows actuelles, telles que le **\_ disque IOCTL \_ obtiennent une \_ \_ géométrie de lecteur** , retournent la taille de secteur logique, mais la taille de secteur physique peut être récupérée par le biais du code de contrôle de [ \_ \_ \_ propriété de requête de stockage IOCTL](/windows-hardware/drivers/ddi/content/ntddstor/ni-ntddstor-ioctl_storage_query_property) , avec les informations pertinentes contenues dans le champ **BytesPerPhysicalSector** de la structure du [ \_ \_ \_ descripteur d’alignement de l’accès au stockage](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor) . Ce sujet est abordé plus en détail plus loin dans cet article.

## <a name="initial-types-of-large-sector-media"></a>Types initiaux des médias de grands secteurs

Le secteur du stockage est rapidement en train de migrer vers ce nouveau type de stockage avancé pour les médias avec des tailles de secteur physique de 4 Ko. Deux types de médias seront publiés sur le marché :

-   **4 Ko natifs**: ce support n’a pas de couche d’émulation et expose directement 4 Ko comme taille de secteur logique et physique. Ce support n’est actuellement pas pris en charge par Windows et la plupart des autres systèmes d’exploitation. Toutefois, Microsoft effectue une investigation sur la faisabilité de la prise en charge de ce type de média dans une future version de Windows et émet un article de la base de connaissances le cas échéant.
-   **émulation de 512 octets (émulation)**: ce média a une couche d’émulation comme indiqué dans la section précédente et expose 512 octets comme taille de secteur logique (semblable à un disque normal aujourd’hui), mais rend ses informations de taille de secteur physique (4 Ko) disponibles. C’est ce que plusieurs fournisseurs de stockage sont actuellement en train d’introduire sur le marché. Ce problème global avec ce nouveau type de média est que la majorité des applications et des systèmes d’exploitation ne comprennent pas l’existence de la taille de secteur physique, ce qui peut entraîner un certain nombre de problèmes, comme indiqué ci-dessous.

## <a name="how-emulation-works-read-modify-write-rmw"></a>Fonctionnement de l’émulation : lecture-modification-écriture (RMW)

Un support de stockage a une certaine unité dans laquelle le support physique peut être modifié. Autrement dit, le support peut uniquement être écrit, ou réécrit, dans des unités de la taille de secteur physique. Par conséquent, les écritures qui ne sont pas exécutées à ce niveau d’unité nécessitent des étapes supplémentaires, que nous allons examiner dans l’exemple suivant.

Dans ce scénario, une application doit mettre à jour le contenu d’un enregistrement DataStor situé dans un secteur logique de 512 octets. Le diagramme suivant illustre les étapes nécessaires pour que le périphérique de stockage termine l’écriture :

![étapes nécessaires à la mise à niveau d’un enregistrement DataStor dans un secteur logique de 512 octets](images/512ermwsteps.png)

Comme illustré ci-dessus, ce processus implique un travail du dispositif de stockage qui peut entraîner une perte de performances. Pour éviter ce travail supplémentaire, les applications doivent être mises à jour pour effectuer les opérations suivantes :

-   Recherchez la taille de secteur physique.
-   Vérifiez que les écritures sont alignées sur la taille de secteur physique indiquée.

## <a name="the-resiliency-impact-of-read-modify-write"></a>Impact de la résilience de lecture-modification-écriture

La résilience permet à une application de récupérer l’état entre les sessions. Nous avons vu ce qui est nécessaire pour qu’un dispositif de stockage émulation effectue une écriture de secteur de 512 octets : le cycle de lecture-modification-écriture. Examinons ce qui se passerait si le processus de remplacement du secteur physique précédent sur le support était interrompu. Quelles sont les conséquences ?

-   Étant donné que la plupart des lecteurs de disque dur mettent à jour sur place, le secteur physique, c’est-à-dire la partie du support où se trouvait le secteur physique, aurait pu être endommagé avec des informations incomplètes en raison d’un remplacement partiel. En d’autres termes, vous pouvez le considérer comme susceptible d’avoir perdu les 8 secteurs logiques que le secteur physique contient logiquement.

-   Alors que la plupart des applications avec un magasin de données sont conçues avec la possibilité de récupérer à partir d’erreurs de support, la perte de huit secteurs ou d’une autre façon, la perte de huit enregistrements de validation, peut potentiellement empêcher la récupération normale de la Banque de données. Un administrateur peut avoir besoin de restaurer manuellement la base de données à partir d’une sauvegarde ou de devoir effectuer une reconstruction longue.

-   Un impact plus important est que l’acte d’une autre application entraînant un cycle de lecture-modification-écriture peut potentiellement entraîner la perte de vos données, même si votre application n’est pas en cours d’exécution ! Cela est tout simplement dû au fait que vos données et les données de l’autre application peuvent se trouver dans le même secteur physique.

En tenant compte de cela, il est important que les logiciels d’application réévaluent les hypothèses prises dans le code et qu’ils soient conscients de la distinction entre la taille des secteurs physiques et logiques, ainsi que certains scénarios clients intéressants décrits plus loin dans cet article.

Ce problème est plus susceptible de se produire si votre application s’appuie sur une banque de données de structure de journaux.

## <a name="avoiding-read-modify-write"></a>Éviter la lecture-modification-écriture

Alors que certains fournisseurs de stockage peuvent introduire des niveaux d’atténuation au sein de certains dispositifs de stockage émulation pour essayer de faciliter les problèmes de performances et de résilience du cycle de lecture-modification-écriture, il n’y a que peu d’atténuation pouvant être gérée en termes de charge de travail. Par conséquent, les applications ne doivent pas s’appuyer sur cette atténuation comme une solution à long terme.

La solution à cela n’est pas une atténuation dans le lecteur, mais pour que les applications fassent le bon ensemble de choses pour éviter le cycle de lecture-modification-écriture. Cette section décrit les scénarios courants dans lesquels les applications peuvent rencontrer des problèmes avec les disques de secteurs importants et suggère un moyen d’investigation pour essayer et résoudre chaque problème.

### <a name="issue-1-the-partition-is-not-aligned-to-a-physical-sector-boundary"></a>Problème 1 : la partition n’est pas alignée sur une limite de secteur physique

Lorsque l’administrateur/l’utilisateur partitionne le disque, la première partition n’a peut-être pas été créée sur une limite alignée. Cela peut entraîner la non-alignement de toutes les écritures suivantes sur les limites du secteur physique. À compter de Windows Vista SP1 et de Windows Server 2008, la première partition est placée au premier 1024 Ko du disque (pour les disques 4 Go ou plus, sinon l’alignement est de 64 Ko) qui est aligné sur une limite de secteur physique de 4 Ko. Toutefois, étant donné le partitionnement par défaut dans Windows XP, un utilitaire de partitionnement tiers ou une utilisation incorrecte des API Windows, les partitions créées peuvent ne pas être alignées sur une limite de secteur physique. Les développeurs doivent s’assurer que les API correctes sont utilisées pour garantir l’alignement. Les API recommandées pour garantir l’alignement des partitions sont décrites ci-dessous.

Les API **IVdsPack :: CreateVolume** et **IVdsPack2 :: CreateVolume2** n’utilisent pas le paramètre d’alignement spécifié lorsqu’un nouveau volume est créé, et utilisent à la place la valeur d’alignement par défaut pour le système d’exploitation (pré-Windows Vista SP1 utilise 63 octets et la version ultérieure de Windows Vista SP1 utilise les valeurs par défaut indiquées ci-dessus). Par conséquent, il est recommandé que les applications qui doivent créer des partitions utilisent les API **IVdsCreatePartitionEx :: CreatePartitionEx** ou **IVdsAdvancedDisk :: CreatePartition** à la place, qui utilisent le paramètre d’alignement spécifié.

La meilleure façon de s’assurer que l’alignement est correct est de le faire juste lors de la création initiale de la partition. Dans le cas contraire, votre application devra prendre en compte l’alignement lors de l’exécution d’écritures ou de l’initialisation, ce qui peut être très complexe. À compter de Windows Vista SP1, ce n’est généralement pas un problème. Toutefois, les versions antérieures de Windows peuvent créer des partitions non alignées qui peuvent entraîner des problèmes de performances avec certains disques de format avancé.

### <a name="issue-2-unbuffered-writes-not-aligned-to-physical-sector-size"></a>Problème 2 : écritures non mises en mémoire tampon non alignées sur la taille de secteur physique

Le problème de base est que les écritures non mises en mémoire tampon ne sont pas alignées sur la taille de secteur physique indiquée du support de stockage, ce qui déclenche une lecture-modification-écriture dans le lecteur qui peut entraîner des problèmes de performances. Les écritures mises en mémoire tampon, en revanche, sont alignées sur la taille de la page, soit 4 Ko, ce qui est par conséquent la taille de secteur physique de la première génération de médias de grands secteurs. Toutefois, la plupart des applications avec un magasin de données effectuent des écritures non mises en mémoire tampon et doivent donc s’assurer que ces écritures sont effectuées dans des unités de la taille de secteur physique.

Pour déterminer si votre application émet des e/s non mises en mémoire tampon, vérifiez que vous incluez l’indicateur de **fichier aucun indicateur de \_ mise en \_ \_ mémoire tampon** dans le paramètre *DwFlagsAndAttributes* lorsque vous appelez la fonction **CreateFile** .

En outre, si vous alignez actuellement les écritures sur la taille de secteur, cette taille de secteur est très probablement la taille de secteur *logique* , car la plupart des API existantes qui interrogent la taille de secteur du média interrogent vraiment l’unité d’adressage, c’est-à-dire la taille de secteur logique. La taille de secteur d’intérêt ici est la taille de secteur physique, qui est l’unité réelle d’atomicité. Voici quelques exemples d’API qui récupèrent la taille de secteur logique :

-   **GetDiskFreeSpace**, **GetDiskFreeSpaceEx**
-   **FileFsVolumeInformation**
-   **IOCTL \_ DISQUE \_ Obtient \_ la \_ géométrie du lecteur**, **IOCTL \_ Disk obtient la géométrie du \_ \_ lecteur \_ \_ ex**
-   **IVdsDisk :: GetProperties**, **IVdsDisk3 :: GetProperties2**

**Comment interroger la taille de secteur physique**

Microsoft a fourni un exemple de code sur MSDN détaillant comment une application peut interroger la taille de secteur physique du volume. L’exemple de code se trouve à l’emplacement <https://msdn.microsoft.com/library/ff800831.aspx> .

Bien que l’exemple de code ci-dessus vous permette d’obtenir la taille de secteur physique du volume, vous devez effectuer une vérification de l’intégrité de base sur la taille de secteur physique indiquée avant de l’utiliser, car il a été observé que certains pilotes peuvent ne pas retourner des données correctement mises en forme :

-   Assurez-vous que la taille de secteur physique indiquée est >= la taille de secteur logique signalée. Si ce n’est pas le cas, votre application doit utiliser une taille de secteur physique égale à la taille de secteur logique signalée.
-   Assurez-vous que la taille de secteur physique indiquée est une puissance de deux. Si ce n’est pas le cas, votre application doit utiliser une taille de secteur physique égale à la taille de secteur logique signalée.
-   Si la taille de secteur physique est une valeur Power-of-Two comprise entre 512 octets et 4 Ko, vous devez envisager d’utiliser une taille de secteur physique arrondie à la taille de secteur logique signalée.
-   Si la taille de secteur physique est une valeur Power-of-Two supérieure à 4 Ko, vous devez évaluer la capacité de votre application à gérer ce scénario avant d’utiliser cette valeur. Dans le cas contraire, vous devez envisager d’utiliser une taille de secteur physique arrondie à 4 Ko.

L’utilisation de cette IOCTL pour obtenir la taille de secteur physique présente plusieurs limites :

-   Requiert des privilèges élevés. Si votre application ne s’exécute pas avec des privilèges, vous devrez peut-être écrire une application de service Windows comme indiqué ci-dessus.

-   Ne prend pas en charge les volumes SMB. Vous devrez peut-être également écrire une application de service Windows pour prendre en charge l’interrogation de la taille des secteurs physiques sur ces volumes.

-   Ne peut pas être émis pour un handle de fichier (l’IOCTL doit être délivré à un handle de volume).

-   Pris en charge uniquement dans les versions de Windows mentionnées au début de cet article.

**Les enregistrements de validation sont remplis pour les secteurs de 512 octets**

Les applications avec un magasin de données ont généralement une forme d’enregistrement de validation qui conserve les informations sur les modifications des métadonnées ou gère la structure du magasin de données. Pour éviter que la perte d’un secteur n’affecte plusieurs enregistrements, cet enregistrement de validation est généralement rempli à une taille de secteur. Avec un disque avec une plus grande taille de secteur physique, l’application doit interroger la taille de secteur physique comme indiqué dans la section précédente et vérifier que chaque enregistrement de validation est rempli à cette taille. Non seulement cela évite le cycle de lecture-modification-écriture, mais il permet de s’assurer qu’en cas de perte d’un secteur physique, un seul enregistrement de validation est perdu.

**Les fichiers journaux sont écrits dans des blocs non alignés**

Les e/s non mises en mémoire tampon sont généralement utilisées lors de la mise à jour ou de l’ajout d’un fichier journal. Il existe plusieurs façons de s’assurer que ces mises à jour sont correctement alignées :

-   Mettre à jour en interne les journaux des mises à jour de la taille de secteur physique indiquée du support d’exploitation et émettre des écritures de journal uniquement lorsqu’une unité de secteur physique est pleine
-   Utiliser des e/s mises en mémoire tampon

### <a name="issue-3-file-formats-relying-on-512-byte-sectors"></a>Problème 3 : formats de fichiers basés sur des secteurs de 512 octets

Certaines applications avec des formats de fichier standard (tels que VHD 1,0) peuvent avoir des fichiers codés en dur pour supposer une taille de secteur de 512 octets. Ainsi, les mises à jour et les écritures dans ce fichier entraîneraient un cycle de lecture-modification-écriture sur l’appareil, ce qui peut entraîner des problèmes de performances et de résilience pour vos clients. Toutefois, il existe des moyens pour une application d’assurer la prise en charge de l’utilisation de ce type de média, par exemple :

-   Utilisez la mise en mémoire tampon pour vous assurer que les écritures sont effectuées dans les unités de la taille de secteur physique
-   Implémentez une lecture-modification-écriture interne qui peut aider à garantir que les mises à jour sont effectuées dans les unités de la taille de secteur physique indiquée.
-   Si possible, compléter les enregistrements dans un secteur physique, de telle sorte que le remplissage soit interprété comme un espace vide
-   Envisagez de reconcevoir une nouvelle version de la structure de données de l’application avec prise en charge des secteurs plus grands

### <a name="issue-4-the-reported-physical-sector-size-can-change-between-sessions"></a>Problème 4 : la taille de secteur physique signalée peut changer d’une session à l’autre

Il existe de nombreux scénarios dans lesquels la taille de secteur physique signalée du stockage sous-jacent qui héberge le DataStor peut changer. Le plus souvent, c’est lorsque vous migrez le DataStor vers un autre volume, ou même sur le réseau. Une modification de la taille de secteur physique signalée peut être un événement inattendu pour de nombreuses applications et peut potentiellement entraîner l’échec de la réinitialisation de certaines applications.

Il ne s’agit pas du scénario le plus simple pour prendre en charge et est mentionné ici comme un avis. Vous devez prendre en compte les besoins de mobilité de vos clients et ajuster votre support en conséquence pour vous assurer que les clients ne sont pas affectés négativement à l’aide d’un média émulation.

## <a name="4-kb-native-media"></a>Support natif de 4 Ko

le support d’émulation de 512 octets est une étape de transition entre le support natif de 512 octets et le média natif de 4 Ko. nous pensons que le support natif de 4 Ko a été publié peu de temps après la disponibilité de émulation. Il y a plusieurs implications importantes avec ce support, qui doivent être notées :

-   Les tailles de secteur logique et physique sont toutes les deux de 4 Ko
-   Étant donné qu’il n’existe aucune couche d’émulation, les écritures non alignées sont en échec par le stockage
-   Aucune résilience cachée : les applications fonctionnent ou elles ne fonctionnent pas

Même si Microsoft étudie actuellement la prise en charge de ces types de médias dans une future version de Windows et émet un article de la base de connaissances le cas échéant, les développeurs d’applications doivent prendre en compte la prise en charge de ces types de médias.

## <a name="closing"></a>Fermeture

Dans cet article, nous avons abordé les conséquences de la présentation de nombreux supports de grands secteurs avec un grand nombre de scénarios de déploiement courants. Nous avons vu l’impact des performances et de la résilience sur la lecture-modification-écriture, certains des scénarios intéressants que ce support peut introduire, et l’ensemble des problèmes qu’ils peuvent potentiellement causer avec les logiciels, ce qui affecte finalement l’utilisateur final. Le secteur du stockage est rapidement transféré vers des supports avec des tailles de secteur supérieures, et les clients ne seront pas en mesure d’acheter des disques avec des tailles de secteur de 512 octets traditionnelles.

Il s’agit d’un document vivant qui est destiné aux développeurs pour mieux comprendre cette transition. Vous devez entamer une conversation avec vos organisations respectives, avec les clients, les professionnels de l’informatique et les fournisseurs de matériel pour discuter de la transition de secteurs importants et de la façon dont elle affecte les scénarios qui sont importants pour vous.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   **Déclaration de support générale de Windows**: <https://support.microsoft.com/kb/2510009>
-   **Correctif logiciel pour Windows 7 et Windows Server 2008 R2**: <https://support.microsoft.com/kb/982018>
-   **Correctif pour Windows Vista et Windows Server 2008**: <https://support.microsoft.com/kb/2470478>
-   **Instruction de prise en charge HyperV**: <https://support.microsoft.com/kb/2515143>
-   **Informations générales sur l’IOCTL \_ \_Code de \_ contrôle de propriété de requête de stockage**: [https://msdn.microsoft.com/library/ff560590.aspx](/windows-hardware/drivers/ddi/ntddstor/ni-ntddstor-ioctl_storage_query_property)
-   **IOCTL \_ \_Code de \_ contrôle de propriété de requête de stockage**: [https://msdn.microsoft.com/library/ff800830.aspx](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property)
-   **Informations générales sur le stockage \_ \_Structure du \_ descripteur d’alignement d’accès**: [https://msdn.microsoft.com/library/ff566344.aspx](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-_storage_access_alignment_descriptor)
-   **Description de la terminologie standard utilisée pour décrire les mises à jour logicielles Microsoft**: <https://support.microsoft.com/kb/824684/>
-   **Exemple de code WDK** avec des détails sur la façon d’extraire les informations d’alignement de l’accès de stockage signalées à partir de la structure du **\_ \_ \_ descripteur d’alignement** de l’accès au stockage lors d’un appel au code de contrôle de **propriété de \_ requête de stockage \_ \_ IOCTL** : [/Windows/Desktop/API/winioctl/NS-winioctl-STORAGE_ACCESS_ALIGNMENT_DESCRIPTOR](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor)
-   **Informations générales sur les options d’imagex Command-Line**: <https://technet.microsoft.com/library/dd799302(WS.10).aspx>
-   **Pilotes de chipset Intel requis pour prendre en charge les lecteurs de secteur de 4 Ko**: <https://www.intel.com/support/chipsets/imsm/sb/CS-031502.htm>
-   Pour plus d’informations sur les disques au format avancé, visitez les IDEMs sites Web suivants :
    -   <http://idema.org/?page_id=2172>
    -   <http://idema.org/?download=7926>

 

 
