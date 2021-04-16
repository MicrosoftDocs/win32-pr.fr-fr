---
description: Décrit la cohérence des lectures validées, l’isolation de lecture validée et les concepts de verrouillage transactionnel dans NTFS transactionnel.
ms.assetid: 18579c4a-a832-4c89-8fb1-cd2542e4375e
title: Concepts de base de TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f2f5d0885795f20a8dfb5e0963468ff04bb8e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320105"
---
# <a name="basic-txf-concepts"></a>Concepts de base de TxF

## <a name="read-isolation"></a>Isolation de lecture

NTFS transactionnel (TxF) fournit une cohérence en lecture validée.

Un [*rédacteur transactionnel*](glossary.md) fait référence à un descripteur de fichier transactionnel ouvert avec une autorisation qui ne fait pas partie d’un accès en lecture générique, mais qui fait partie d’un accès en écriture générique. Un *rédacteur transactionnel* affiche la version la plus récente d’un fichier qui comprend toutes les modifications apportées par la même transaction. Il ne peut y avoir qu’un seul Writer traité par fichier. Les rédacteurs non transactionnels sont toujours bloqués par un rédacteur transactionnel, même si le fichier est ouvert avec des autorisations en écriture partagée.

Un [*lecteur transactionnel*](glossary.md) fait référence à un descripteur de fichier transactionnel ouvert avec une autorisation qui fait partie de l’accès en lecture générique, mais qui ne fait pas partie d’un accès en écriture générique. Un *lecteur traité* affiche une version validée du fichier qui existait au moment où le descripteur de fichier a été ouvert. Le lecteur traité est isolé des effets des enregistreurs traités. Cela fournit une vue cohérente du fichier uniquement pendant la durée de vie du descripteur de fichier et bloque les enregistreurs non transactionnels.

> [!Note]  
> Lorsqu’un descripteur a été ouvert en vue d’une modification avec la fonction [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) , toutes les ouvertures suivantes du fichier au sein de cette transaction, qu’il soit en lecture seule ou non, sont converties par le système en rédacteur transactionnel à des fins d’isolation et d’autres sémantiques transactionnelles. Cela signifie que, quand un handle est ouvert pour l’accès en lecture seule, le handle ne reçoit pas de vue du fichier avant le début de la transaction ; elle reçoit la vue de la transaction active du fichier.

 

Un descripteur de fichier non transactionnel ne voit pas les modifications apportées dans une transaction tant que la transaction n’est pas validée. Le descripteur de fichier non transactionnel reçoit une vue isolée qui est similaire à un lecteur traité, mais contrairement à un lecteur traité, il reçoit la mise à jour du fichier lorsqu’un rédacteur transactionnel valide la transaction.

## <a name="isolation-levels"></a>Niveaux d’isolation

TxF offre une isolation en lecture validée. Cela signifie que les mises à jour de fichiers ne sont pas visibles en dehors de la transaction. En outre, si un fichier est ouvert plusieurs fois lors de la lecture de fichiers dans la transaction, vous pouvez voir des résultats différents avec chaque ouverture suivante. Les fichiers qui étaient disponibles lors de leur première accès peuvent ne pas être disponibles (car ils ont été supprimés), ou vice versa.

## <a name="transactional-locking"></a>Verrouillage transactionnel

La création d’un rédacteur transactionnel sur un fichier verrouille de façon *transactionnelle* le fichier. Une fois qu’un fichier est verrouillé par une transaction, les autres opérations du système de fichiers externes à la transaction de verrouillage qui tentent de modifier le fichier verrouillé de manière transactionnelle échouent avec une **\_ \_ violation de partage des erreurs** ou un **\_ \_ conflit transactionnel d’erreur**.

Le tableau suivant résume le verrouillage transactionnel.



Fichier actuellement ouvert par

Fichier ouvert tenté par

Transacted

Non transactionnel

Lecteur

Lecteur/enregistreur

Lecteur

Lecteur/enregistreur

Lecteur transactionnel

Oui

Oui

Oui

Non 2

Lecteur/enregistreur transactionnel

Oui

Non 2

Oui

Non 2

Lecteur non transactionnel

Oui

Oui

Oui

Oui

Lecteur/enregistreur non transactionnel

Non1

Non1

Oui

Oui

1. Échec avec **\_ \_ conflit transactionnel d’erreur**<br/> 2. échec avec **\_ \_ violation de partage d’erreurs**<br/>



 

Si vous ouvrez un flux nommé pour une modification qui utilise une transaction, la totalité du fichier doit être verrouillée.

En plus du verrouillage transactionnel, les règles de partage de fichiers NTFS standard s’appliquent.

Vous devez prendre en compte les deux modes de partage de fichiers suivants en parallèle :

-   Mode de verrouillage transactionnel.
-   Modes de partage de fichiers normaux.

Quel que soit le mode le plus restrictif, c’est celui qui s’applique.

 

 




