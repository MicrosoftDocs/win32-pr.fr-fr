---
description: Flux audio et sous-image
ms.assetid: 8d361da3-a33a-401c-a750-f9b952022cf6
title: Flux audio et sous-image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f5c8c74f7507557f374d690a671b62e8b43343
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482536"
---
# <a name="audio-and-subpicture-streams"></a>Flux audio et sous-image

Un disque DVD-Video peut avoir jusqu’à huit flux audio, numérotés de 0 à 7, chacun avec jusqu’à six canaux discrets. (Notez que les flux audio et de sous-image sont numérotés à partir de zéro, tandis que les titres, les angles et les niveaux parental sont numérotés à partir de un.) Vous ne pouvez sélectionner qu’un seul de ces flux à un moment donné. Pour les sous-images, jusqu’à 32 flux sont disponibles, bien qu’un seul flux puisse être activé à un moment donné. Les disques sont généralement créés avec des flux audio et sous-images par défaut, mais une application peut permettre aux utilisateurs d’afficher la liste de tous les flux disponibles et de sélectionner celle-ci dans la langue de leur choix. Les étapes de base de ce processus sont les mêmes pour les flux audio et de sous-image.

1.  Déterminez le nombre de flux disponibles pour un titre.
2.  Itérez au sein des flux et récupérez les attributs de flux pour chacun.
3.  Récupérez le code de langue de l’identificateur de paramètres régionaux (LCID) retourné et créez une chaîne explicite.
4.  Remplir une zone de liste ou un autre contrôle de l’interface utilisateur pour permettre à l’utilisateur de sélectionner un flux préféré.

Dans l’exemple d’application de DVD, la méthode CAudioLangDlg :: MakeAudioStreamList dans Dialogs. cpp illustre les étapes de base.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> </dl>

 

 



