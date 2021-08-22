---
title: Formats de données et média de transfert
description: Formats de données et média de transfert
ms.assetid: c6023c42-ce20-40e4-9d88-55fa1d2a4d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ccbab96fbaca83330737521f253b3c625e67ea9a024d87d35276da2826a3964
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501429"
---
# <a name="data-formats-and-transfer-media"></a>Formats de données et média de transfert

la plupart des plateformes, y compris les Windows, définissent un protocole standard pour transférer des données entre les applications, en fonction d’un ensemble de fonctions appelé le presse-papiers. Les applications qui utilisent ces fonctions peuvent partager des données même si leurs formats de données natifs sont très différents. En règle générale, ces presse-papiers présentent deux lacunes importantes que COM a résolues.

tout d’abord, les descriptions de données utilisent uniquement un identificateur de format, tel que l’identificateur de format du presse-papiers 16 bits unique sur Windows, ce qui signifie que le presse-papiers peut uniquement décrire la structure de ses données, c’est-à-dire le classement des bits. Il peut créer un rapport, « j’ai une bitmap « » ou j’ai du texte», mais il ne peut pas spécifier les appareils cibles pour lesquels les données sont composées, les vues ou les aspects des données qu’ils peuvent fournir, ou les supports de stockage les mieux adaptés à son transfert. Par exemple, il ne peut pas créer de rapport, « j’ai une chaîne de texte qui est stockée dans la mémoire globale et mise en forme pour une présentation à l’écran ou sur une imprimante » ou « j’ai une bitmap d’esquisse miniature restituée pour une imprimante à matrice à 100 ppp et stockée sous forme de fichier de disque ».

Deuxièmement, tous les transferts de données à l’aide du presse-papiers se produisent généralement via la mémoire globale. L’utilisation de la mémoire globale est raisonnablement efficace pour les petites quantités de données, mais littéralement inefficace pour des volumes importants, tels qu’un objet multimédia de 20 Mo. La mémoire globale est lente pour un objet de données volumineux, dont la taille nécessite une permutation importante de la mémoire virtuelle sur le disque. Dans les cas où les données qui sont échangées se trouvent principalement sur le disque, leur forçage dans ce goulot d’étranglement de la mémoire virtuelle est très inefficace. Une meilleure méthode consiste à ignorer la mémoire globale entièrement et à transférer simplement les données directement sur le disque.

Pour atténuer ces problèmes, COM fournit deux structures de données : [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) et [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1). Pour plus d'informations, voir les rubriques suivantes :

-   [La structure FORMATETC](the-formatetc-structure.md)
-   [La structure STGMEDIUM](the-stgmedium-structure.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transfert de données](data-transfer.md)
</dt> </dl>

 

 




