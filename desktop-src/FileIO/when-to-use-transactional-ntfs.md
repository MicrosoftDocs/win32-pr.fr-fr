---
description: Utilisez le NTFS transactionnel pour maintenir l’intégrité des données.
ms.assetid: 886d6075-57e8-47db-aec5-77660d0a53f9
title: Quand utiliser le NTFS transactionnel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022f7a67fe6960a8754f768956457afbd04a509bbf9a3c18360b4651e4d9ccda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830129"
---
# <a name="when-to-use-transactional-ntfs"></a>Quand utiliser le NTFS transactionnel

Une application peut utiliser le NTFS transactionnel (TxF) pour préserver l’intégrité des données sur le disque pendant des conditions d’erreur inattendues. En général, une application doit envisager d’utiliser TxF si l’application vide des fichiers et utilise d’autres techniques pour maintenir l’intégrité des données. TxF peut offrir de meilleures performances et simplifier le code de gestion des erreurs de l’application tout en améliorant la récupération et la fiabilité des erreurs. Les sections suivantes de cette rubrique fournissent des exemples de scénarios d’utilisation de TxF.

## <a name="updating-a-file"></a>Mise à jour d’un fichier

La mise à jour d’un fichier est une opération courante et généralement simple. Toutefois, si le système ou l’application échoue pendant qu’une application met à jour des informations sur un disque, le résultat peut être catastrophique, car les données utilisateur peuvent être endommagées par une opération de mise à jour de fichier qui est partiellement terminée. Les applications robustes exécutent souvent des séquences complexes de copies de fichiers et de renommages de fichiers pour s’assurer que les données ne sont pas endommagées en cas de défaillance d’un système.

TxF permet à une application de protéger facilement les opérations de mise à jour des fichiers en cas de défaillance du système ou de l’application. Pour mettre à jour un fichier en toute sécurité, l’application ouvre le fichier en mode traité, effectue les mises à jour nécessaires, puis valide la transaction. Si le système ou l’application échoue au cours de la mise à jour du fichier, TxF restaure automatiquement le fichier à l’État où il se trouvait avant le début de la mise à jour des fichiers, ce qui évite l’endommagement des fichiers.

## <a name="multi-file-updates"></a>Mises à jour de plusieurs fichiers

TxF est encore plus important quand une seule opération logique affecte plusieurs fichiers. Par exemple, si vous souhaitez utiliser un outil pour renommer l’une des pages HTML ou ASP sur un site Web, un outil bien conçu corrige également tous les liens pour utiliser le nouveau nom de fichier. Toutefois, un échec au cours de cette opération laisse le site Web dans un état incohérent, avec certains liens faisant toujours référence à l’ancien nom de fichier. En faisant de l’opération de changement de nom de fichier et de l’opération de résolution de lien une seule transaction, TxF garantit que le changement de nom de fichier et le correctif de lien réussissent ou échouent comme une seule opération.

## <a name="consistent-concurrent-updates"></a>Mises à jour simultanées cohérentes

TxF isole les transactions simultanées. Si une application ouvre un fichier pour une lecture transactionnelle alors qu’une autre application a le même fichier ouvert pour une mise à jour transactionnelle, TxF isole les effets des deux transactions les unes des autres. En d’autres termes, le lecteur transactionnel affiche toujours une version unique et cohérente du fichier, même si ce fichier est en cours de mise à jour par une autre transaction.

Une application peut utiliser cette fonctionnalité pour permettre aux clients d’afficher les fichiers pendant que d’autres clients effectuent des mises à jour. Par exemple, un serveur Web transactionnel peut fournir une vue unique et cohérente des fichiers, tandis qu’un autre outil met à jour ces fichiers simultanément.

> [!Note]  
> TxF ne prend pas en charge les mises à jour simultanées de plusieurs rédacteurs dans différentes transactions. TxF ne prend en charge qu’un seul enregistreur avec plusieurs lecteurs simultanés et cohérents.

 

## <a name="coordinating-with-other-transacted-resource-managers"></a>Coordination avec d’autres gestionnaires de ressources transactionnelles

Les transactions utilisées avec les systèmes de fichiers traités peuvent également être utilisées avec le registre traité. Les mises à jour apportées au fichier et au Registre sont coordonnées avec une seule transaction.

en utilisant des transactions [Distributed Transaction Coordinator](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC) ou System. transactions, les mises à jour apportées à SQL, MSMQ et d’autres ressources transactionnelles peuvent être coordonnées avec les mises à jour des fichiers traités. Pour plus d’informations, consultez [IKernelTransaction](/previous-versions/windows/desktop/aa344210(v=vs.85))du DTC.

## <a name="unsupported-scenarios"></a>Scénarios non pris en charge

TxF ne prend pas en charge les scénarios de transaction suivants :

-   Transactions sur des volumes réseau, par exemple sur des partages de fichiers. TxF n’est pas pris en charge par les protocoles CIFS/SMB.
-   Transactions sur n’importe quel système de fichiers autre que NTFS.
-   Opérations traitées sur des fichiers mis en cache par la mise en cache côté client.
-   Accès aux fichiers à l’aide des ID d’objet.
-   Tout scénario d’écriture partagée.
-   Toute situation dans laquelle un fichier est ouvert pendant une période prolongée (jours ou semaines).

 

 
