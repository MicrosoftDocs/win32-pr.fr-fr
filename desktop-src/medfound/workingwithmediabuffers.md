---
description: utilisation de mémoires tampons de média DMO
ms.assetid: 6d0c51b8-0d79-4f04-8e90-0cea4f3b1427
title: utilisation de mémoires tampons de média DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c870b3a4a035c71a4dcadf9a38b4c2a150097e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313537"
---
# <a name="working-with-dmo-media-buffers"></a>utilisation de mémoires tampons de média DMO

Les données d’entrée sont transmises au codec DMOs à l’aide de mémoires tampons de média. Une mémoire tampon de média est un objet qui implémente l’interface [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) . vous pouvez implémenter une classe à cet effet ou, si vous utilisez le kit de développement logiciel (sdk) Windows Media Format dans votre application, vous pouvez utiliser les objets de mémoire tampon définis dans ce kit de développement logiciel (sdk).

Si vous implémentez votre propre classe de mémoire tampon, soyez prudent quant à la façon dont la mémoire tampon est gérée. lorsque vous transmettez un exemple d’entrée, le DMO conserve une référence à la mémoire tampon jusqu’à ce qu’elle soit terminée avec l’exemple. Vous pouvez immédiatement libérer votre référence à l’interface [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) , mais vous n’avez aucun moyen de savoir quand le codec n’a plus besoin de sa référence. Pour être certain que la mémoire est libérée lorsque l’objet se supprime lui-même, vous devez implémenter votre classe afin qu’elle alloue et libère la mémoire pour la mémoire tampon en interne.

Étant donné que le DMOs conserve les références aux tampons pendant une période inconnue, il n’est pas facile d’utiliser un pool limité de mémoires tampons. La solution la plus simple consiste à allouer un nouveau tampon pour chaque échantillon, bien que cela soit inefficace.

Une meilleure solution consiste à implémenter un objet pour gérer un pool de mémoires tampons. Pour ce faire, écrivez le code dans la méthode **Release** de votre implémentation de [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) qui appelle une méthode de votre gestionnaire de tampons (au lieu de se supprimer) lorsque le nombre de références est atteint de zéro. Le gestionnaire de tampons peut ensuite gérer une liste de pointeurs vers des objets de mémoire tampon alloués. Créez une méthode dans votre gestionnaire de tampons pour vérifier la liste des mémoires tampons libres et retourner un pointeur afin que votre application puisse accéder aux mémoires tampons si nécessaire. Cette méthode doit créer des mémoires tampons en fonction des besoins et les ajouter à la liste.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
