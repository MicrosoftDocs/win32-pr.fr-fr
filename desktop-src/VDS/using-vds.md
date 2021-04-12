---
description: Utilisation de VDS
ms.assetid: aa4be499-625d-4dbd-828c-4a55ff2dba2c
title: Utilisation de VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c648c5cc2507c4819f98367c367099248a0e723f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210422"
---
# <a name="using-vds"></a>Utilisation de VDS

\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

VDS fournit une interface pour les scripts et le développement d’interface graphique utilisateur qui permet de simplifier les activités effectuées par un administrateur Windows Server qui gère un ensemble hétérogène de systèmes de stockage, en migrant les données entre différentes configurations matérielles dans le temps. Si vous n’êtes pas familiarisé avec les objets utilisés dans le développement VDS, consultez le [modèle d’objet VDS](vds-object-model.md).

Quelques points avant de commencer :

-   Bien que VDS comprenne un fournisseur de logiciels, vous devez acheter un fournisseur de matériel et le matériel associé séparément pour tirer parti des opérations du fournisseur de matériel. Pour obtenir des instructions d’installation, consultez la documentation fournie par le fabricant du matériel.
-   Certaines opérations nécessitent des volumes au format NTFS. Par exemple, lorsque vous montez un volume sur un répertoire existant, le volume qui contient le répertoire doit être formaté avec NTFS. Les autres systèmes de fichiers ne prennent pas en charge cette opération. Pour plus d’informations sur les opérations qui requièrent NTFS, consultez chaque page de méthode dans [référence VDS](vds-reference.md).

## <a name="programming-languages"></a>Langages de programmation

Utilisez n’importe quel langage de programmation adapté au développement avec COM, tel que le langage C ou C++.

## <a name="security"></a>Sécurité

Le pare-feu Windows est activé par défaut. Cela peut entraîner l’échec de l’authentification pour les interfaces de rappel, telles que [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink), qui peuvent être exécutées à distance. Si le pare-feu Windows est activé sur le client ou sur le serveur, vous devez ajouter gestion des volumes à distance sous l’onglet **exceptions** du pare-feu Windows.

**Windows Server 2003 :** Dans Windows Server 2003 avec Service Pack 2 (SP2) et Windows Server 2003 avec Service Pack 1 (SP1), si le pare-feu Windows est activé sur le client ou sur le serveur et si le serveur est configuré pour utiliser l’authentification NTLM, vous devez ajouter les paramètres suivants à l’onglet **exceptions** du pare-feu Windows pour l’ordinateur approprié.

| Computer                 | Paramètres d’exceptions                                                                 |
|--------------------------|-------------------------------------------------------------------------------------|
| Ordinateur client (local)  | Dmremote.exe<br/> Mmc.exe<br/> Vdsldr.exe<br/> TCP 135<br/> |
| Ordinateur serveur (distant) | Dmadmin.exe<br/> Vds.exe<br/> TCP 135<br/>                        |



 

Notez que le pare-feu Windows n’est pas activé par défaut tant que Windows Server 2003 avec SP1 n’est pas installé.

Une application qui utilise VDS doit s’exécuter sous le compte d’opérateur de sauvegarde ou de groupe administrateurs. Sans le privilège approprié, une application peut créer un objet de chargeur de service, mais l’objet ne chargera pas VDS. Au lieu de cela, il retourne une erreur indiquant que l’accès à VDS est refusé.

Si le réseau utilise l’authentification NTLM, l’ordinateur client doit autoriser l’accès anonyme. Dans ce cas, si l’ordinateur client exécute un système d’exploitation Windows Server, l’accès anonyme est activé par défaut. S’il exécute un système d’exploitation client Windows, l’accès anonyme doit être activé à l’aide de Dcomcnfg.exe.

## <a name="configuration-and-query-operations"></a>Opérations de configuration et de requête

Les opérations de configuration et de requête sont délimitées par l’ordinateur, le fournisseur, le sous-système ou le Pack le plus pertinent. Les requêtes traversent uniquement un fournisseur ou un niveau de la hiérarchie de liaison. Pour générer une vue complète, l’appelant doit interroger chaque niveau. La liste suivante comprend des exemples :

-   Pour afficher tous les disques d’un ordinateur, les appelants doivent effectuer une requête sur tous les fournisseurs de logiciels pour les disques revendiqués par ces fournisseurs.
-   Pour déterminer les disques qui contribuent à un volume à pile logicielle, les appelants déterminent d’abord les plex contributeurs, puis interrogent les extensions de disque pour chaque Plex.
-   Pour afficher tous les lecteurs attachés à un sous-système donné, les appelants doivent interroger le sous-système.
-   Pour afficher tous les numéros d’unités logiques qui sont exposés par un sous-système donné, les appelants doivent interroger le sous-système.
-   Pour afficher l’ensemble du stockage sur un réseau SAN ou un cluster, les appelants doivent interroger chaque ordinateur pour tous les fournisseurs de matériel, interroger chaque fournisseur pour tous les sous-systèmes, puis interroger chaque sous-système.

Alors que chaque requête individuelle ne retourne pas de doublons, les requêtes répétées sur les ordinateurs ou parmi les fournisseurs peuvent accumuler les doublons. Les appelants doivent implémenter n’importe quel filtrage. Notez également que les applications de gestion SAN peuvent utiliser le Active Directory ou un référentiel pour rendre persistantes les informations de configuration. Il n’est peut-être pas nécessaire d’interroger chaque ordinateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Service Disque virtuel](virtual-disk-service-portal.md)
</dt> <dt>

[Modèle d’objet VDS](vds-object-model.md)
</dt> <dt>

[Référence VDS](vds-reference.md)
</dt> </dl>

 

