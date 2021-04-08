---
description: 'Une transaction est un groupe d’opérations qui ont les propriétés suivantes : Atomic, cohérent, isolée et durable (ACID).'
ms.assetid: b3da52a3-1c52-4577-a997-7e72ebc03fa8
title: Qu’est-ce qu’une transaction ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c459462d3aee3d7eef556ce0951ede537e8109
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864565"
---
# <a name="what-is-a-transaction"></a>Qu’est-ce qu’une transaction ?

Une transaction est un groupe d’opérations qui ont les propriétés suivantes : Atomic, cohérent, isolée et durable (ACID). La prise en charge des transactions permet de développer de nouveaux types d’applications, tout en simplifiant le processus de développement et en rendant l’application plus robuste. Le reste de cette rubrique fournit des scénarios qui illustrent la nécessité de ces propriétés, puis une table qui définit chaque propriété.

Dans un groupe d’opérations *atomiques* , chaque opération dans le groupe doit être réussie ou les effets de tous doivent être annulés (également appelés *restauration*). Par exemple, un transfert bancaire doit être un ensemble atomique de deux opérations : un débit à partir d’un compte et un crédit à un autre compte. Le débit et le crédit doivent être implémentés en tant que groupe atomique. Si ces deux opérations échouent, le transfert est soit inéquitablement en faveur de la Banque, soit du titulaire du compte.

L’exigence de *cohérence* signifie que les données sont cohérentes après la transaction (en supposant que nous avons commencé avec un système cohérent avant la transaction). Pour l’exemple de transfert bancaire, la cohérence peut être définie de façon à ce que le solde du compte combiné des deux comptes soit une constante. Pour implémenter la cohérence dans l’exemple de transfert bancaire, les opérations de débit et de crédit doivent simplement être destinées à la même somme d’argent.

Une mise à jour d’un site Web constitue un autre exemple de transaction. Un site de commerce électronique exige qu’une nouvelle page de navigation de catégorie de produit apparaisse exactement au même moment que les pages de détails du produit qui décrivent les nouveaux produits. Dans ce cas, il est nécessaire de mettre à jour et d’ajouter plusieurs entrées de répertoire sous le contrôle d’une transaction. Non seulement il est nécessaire que les mises à jour soient atomiques, mais il est également nécessaire qu’un client qui est actuellement en achat ne doive pas voir les mises à jour en cours. Il s’agit d’un exemple de la propriété d' *isolation* des transactions.

La propriété de *durabilité* exige qu’une fois la mise à jour terminée, ses effets persistent même si le système ne répond plus. Dans l’exemple précédent, la durabilité peut être fournie simplement en garantissant une récupération de données adéquate afin que toutes les nouvelles entrées du système de fichiers qui représentent l’ajout d’un nouveau produit au site s’affichent une fois que le système a cessé de répondre. Cela nécessite un système avec des mécanismes de sauvegarde, de récupération et de haute disponibilité des données.

La garantie de l’atomicité d’une transaction, ainsi que des autres propriétés, est présente en ce qui concerne un nombre quelconque d’échecs, y compris les échecs qui se produisent pendant la phase de récupération d’une défaillance précédente. Finalement, le système atteindra l’un des deux États suivants : toutes les opérations ont été appliquées ou aucune des opérations n’a été appliquée.

Les propriétés d’une transaction sont résumées dans le tableau suivant.



| Terme                                                                                                         | Description                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atomique<br/>                 | Soit toutes les opérations de la transaction ont été effectuées, soit aucune des opérations n’est conservée.<br/>                             |
| <span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Conforme<br/> | Si les données sont cohérentes avant le début de la transaction, elles sont cohérentes une fois la transaction terminée.<br/> |
| <span id="Isolated_"></span><span id="isolated_"></span><span id="ISOLATED_"></span>Concerné <br/>     | Les effets d’une transaction en cours sont masqués dans toutes les autres transactions.<br/>                               |
| <span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Durable<br/>             | Lorsqu’une transaction se termine, ses résultats sont persistants et survivent à un incident système.<br/>                               |



 

Ces propriétés garantissent que les logiciels peuvent gérer des erreurs inattendues, car il peut simplement abandonner une transaction lorsqu’une situation inattendue empêche la réussite de son exécution. L’infrastructure de transaction garantit que tous les effets de la transaction abandonnée sont annulés et retournant les données dans un état cohérent. Par conséquent, un système transactionnel permet une récupération normale à partir des défaillances du système.

Pour garantir les propriétés ACID, un système qui prend en charge les transactions doit disposer d’une capacité de journalisation robuste qui peut être utilisée pour valider ou restaurer des transactions si nécessaire. Pour plus d’informations, consultez [Common Log File System](/previous-versions/windows/desktop/clfs/common-log-file-system-portal).

 

