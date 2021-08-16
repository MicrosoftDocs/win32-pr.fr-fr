---
description: Utilisation des mémoires tampons et des exemples de médias MFT
ms.assetid: dda4048e-bc4c-40ac-a6bd-34984f3717e0
title: Utilisation des mémoires tampons et des exemples de médias MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d964f1c2f2a5fd5f92d5af87213c6977fc51bee76caf3a281861788e2a2fb922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736450"
---
# <a name="working-with-mft-media-buffers-and-samples"></a>Utilisation des mémoires tampons et des exemples de médias MFT

Le codec MFTs passe les données multimédias à l’aide des mémoires tampons et des exemples de médias.

Une mémoire tampon de média est un objet COM qui gère un bloc de mémoire, généralement pour contenir des données multimédias. Lorsque des données sont transmises à ou à partir d’une table MFT, elles sont toujours transmises sous la forme d’une mémoire tampon de média.

Toutes les mémoires tampons de média exposent l’interface **IMFMediaBuffer** . Cette interface est conçue pour tous les types de données. Les mémoires tampons contenant des données vidéo exposent souvent **IMF2DBuffer**.

Une mémoire tampon de média a une taille maximale, qui est la quantité de mémoire allouée pour la mémoire tampon. Pour trouver la taille maximale, appelez **IMFMediaBuffer :: GetMaxLength**. À tout moment, une mémoire tampon de support a également une longueur actuelle, qui correspond à la quantité de données valides dans la mémoire tampon, allant de zéro octet jusqu’à la taille maximale. Pour connaître la longueur actuelle, appelez **IMFMediaBuffer :: GetCurrentLength**. Lorsque la mémoire tampon est créée, la longueur actuelle est égale à zéro. Si vous écrivez des données dans la mémoire tampon, appelez **IMFMediaBuffer :: SetCurrentLength** pour mettre à jour la longueur actuelle.

Pour accéder à la mémoire dans la mémoire tampon, appelez **IMFMediaBuffer :: Lock**. Cette méthode retourne un pointeur vers le début du bloc de mémoire. Quand vous avez fini d’utiliser le pointeur, appelez **IMFMediaBuffer :: Unlock**. La méthode **Lock** n’est pas un mécanisme de synchronisation de threads. Cela ne garantit pas que les autres threads ne peuvent pas accéder à la mémoire tampon. La méthode **Lock** est utilisée pour s’assurer que l’accès à la mémoire reste valide jusqu’à ce que vous appeliez la méthode **Unlock** .

Un exemple d’objet multimédia (dans le contexte du kit de développement logiciel (SDK) Media Foundation) est un objet qui contient une liste triée de zéro ou plusieurs mémoires tampons. Les exemples de supports exposent l’interface **IMFSample** .

Pour créer un nouvel exemple, appelez la fonction **MFCreateSample** . Initialement, la liste de mémoires tampons de l’exemple est vide. Pour ajouter une mémoire tampon à la fin de la liste, appelez **IMFSample :: AddBuffer**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du codec DMOs](workingwithcodecdmos.md)
</dt> <dt>

[Utilisation du codec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



