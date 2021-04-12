---
title: Éviter le polymorphisme
description: Les nouveaux types de données incluent deux types polymorphes, INT \_ PTR et long \_ ptr.
ms.assetid: 3d18016d-772c-45bc-8057-7281e71a8707
keywords:
- Programmation Windows de polymorphisme 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec0fd26944d58a9ba0d253da8b8dbcd68156436
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311104"
---
# <a name="avoiding-polymorphism"></a>Éviter le polymorphisme

Les nouveaux types de données incluent deux types polymorphes, **int \_ ptr** et **long \_ ptr**. Sur Windows 32 bits, le **\_ ptr int** est mappé à **int** et le **\_ ptr long** est mappé à **long**. Sur Windows 64 bits, les deux types sont mappés au type intrinsèque **\_ \_ Int64** . Le compilateur MIDL prend en charge ces types pour les appels de procédure distante, mais il existe une limitation inhérente que vous devez garder à l’esprit lorsque vous les utilisez dans un environnement distribué. Veillez à commenter votre code en conséquence.

Quelle que soit la taille de la plateforme, la taille du câble de ces types polymorphes est toujours de 32 bits. Lors du démarshaling sur Windows 64 bits, la signature de la bibliothèque Runtime étend les valeurs signées et assigne zéro aux octets de poids fort pour une valeur non signée. Lorsque vous mettez une valeur 64 bits sur le câble, le temps d’exécution tronque les octets de poids fort. Ainsi, seules les valeurs 32 bits de poids faible sont utilisables.

Utilisez les types polymorphes uniquement lorsque cela est nécessaire pour le portage. Pour les nouvelles interfaces, utilisez les types d’entiers intrinsèques MIDL **\_ \_ Int32** et **\_ \_ Int64**, ou utilisez un type pointeur ou un handle de contexte, selon la valeur la plus appropriée pour le type de données transférées.

Le compilateur 64 bits prend en charge un nouveau **\_ \_ int3264** intrinsèque polymorphe. Là encore, ce type a été développé pour prendre en charge les efforts de Portage, dans ce cas pour prendre en charge les types **\_ ptr PTR** en toute transparence. (Un autre intrinsèque, **\_ \_ long3264**, prendra en charge le type **\_ ptr ulong** .) N’utilisez pas directement **\_ \_ int3264** ; utilisez le type de **\_ pointeur int** lorsque vous avez besoin d’un type polymorphe pour des raisons de Portage.

 

 




