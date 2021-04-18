---
description: Il peut s’avérer nécessaire d’arrêter un service avant et redémarré à la suite d’une opération de restauration.
ms.assetid: 111d1281-ad83-49bc-868c-1106a0e25a2a
title: Arrêt des services pour la restauration par les demandeurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548af25a4b4550d35a8e6fa4d4c0e791897b6e0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533872"
---
# <a name="stopping-services-for-restore-by-requesters"></a>Arrêt des services pour la restauration par les demandeurs

Il peut s’avérer nécessaire d’arrêter un service avant et redémarré à la suite d’une opération de restauration.

En règle générale, l’arrêt et le démarrage d’un service pour prendre en charge une restauration sont effectués par un enregistreur lors du traitement de l’événement de [*prérestauration*](vssgloss-p.md) (avec [**CVssWriter :: OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)) et de l’événement [*postRestore*](vssgloss-p.md) (avec [**CVssWriter :: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)).

Toutefois, dans certains cas, il peut être nécessaire qu’un demandeur arrête explicitement un service en cours d’exécution. Les enregistreurs indiquent si c’est le cas en définissant la \_ valeur VSS RME \_ Stop \_ Restore \_ Start ou VSS \_ RME \_ Restore \_ Stop \_ Start de l’énumération [**VSS \_ RESTOREMETHOD \_ enum**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) comme argument de la méthode Restore d’un appel à la méthode [**IVssCreateWriterMetadata :: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) et en spécifiant le nom du service à arrêter.

Un demandeur obtient des informations sur la méthode de restauration et le nom du service à arrêter lors de l’utilisation des métadonnées de l’enregistreur à l’aide de la méthode [**IVssExamineWriterMetadata :: GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod) .

Il est important que le rédacteur, lorsque vous spécifiez le nom d’un service à arrêter, utilise le nom public correct de ce service. Un nom ambigu ou inexact peut entraîner l’arrêt d’un service incorrect par les demandeurs ou l’incapacité à déterminer quel service arrêter.

Une fois l’opération de restauration terminée, les demandeurs doivent redémarrer le service.

Vous devez être prudent lors de la conception et de l’implémentation d’enregistreurs qui prennent en charge les services que les demandeurs doivent arrêter et redémarrer. En particulier, ces Writers ne doivent pas faire partie du service, autrement dit, l’enregistreur lui-même ne doit pas nécessairement être arrêté, puis redémarré au cours de l’opération de restauration.

Un enregistreur dont le processus est arrêté aura une instance de writer différente lors du redémarrage. La nouvelle instance du writer ne recevra pas les événements VSS destinés à l’instance d’origine du writer. Plus précisément, si le processus d’une instance de writer est arrêté après la gestion d’un événement de prérestauration, la nouvelle instance ne recevra pas l’événement PostRestore. En outre, VSS génère une erreur indiquant la perte d’un writer participant dans l’opération de restauration, et [**IVssBackupComponents ::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) peut retourner un échec.

 

 



