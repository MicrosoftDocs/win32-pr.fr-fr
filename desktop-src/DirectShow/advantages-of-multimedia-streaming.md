---
description: Avantages de la diffusion multimédia en continu
ms.assetid: 01020ad5-430d-4b4d-8de3-bcc81270e132
title: Avantages de la diffusion multimédia en continu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06df23ce833462aee9b7d4b3840c1fae2d4f3b15c4ee6daee2e4a421259493a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537539"
---
# <a name="advantages-of-multimedia-streaming"></a>Avantages de la diffusion multimédia en continu

> [!Note]  
> Ces API sont déconseillées. les Applications doivent utiliser le filtre d' [**accrochage d’exemple**](sample-grabber-filter.md) ou implémenter un filtre personnalisé pour obtenir des données à partir d’un graphique de filtre DirectShow.

 

Lorsque les développeurs utilisent la diffusion multimédia en continu dans leurs applications, cela réduit considérablement la quantité de programmation spécifique au format nécessaire. En règle générale, une application qui doit obtenir des données multimédias à partir d’une source de fichier ou matérielle doit tout savoir sur le format des données et sur le périphérique matériel. L’application doit gérer la connexion, le transfert de données, toute conversion de données nécessaire et le rendu de données ou le stockage de fichiers réel. Étant donné que chaque format et appareil est légèrement différent, ce processus est souvent complexe et fastidieux. La diffusion multimédia en continu, en revanche, négocie automatiquement le transfert et la conversion des données de la source vers l’application. Les interfaces de streaming fournissent une méthode uniforme et prévisible d’accès et de contrôle des données, ce qui permet à une application de lire facilement les données, quelle que soit leur source ou leur format d’origine.

Les étapes suivantes montrent comment implémenter la diffusion en continu, d’un périphérique matériel à un rendu de lecture.

1.  une source de données vidéo, telle que DirectShow, expose les interfaces de streaming.
2.  Le développeur d’applications utilise les interfaces de diffusion multimédia en continu pour gérer la conversion de format de données.
3.  Le développeur d’applications utilise les interfaces DirectDraw pour afficher les données résultantes.

La spécification des flux multimédias comprend plusieurs interfaces. chaque interface comprend des méthodes qui contrôlent un certain aspect du processus de diffusion en continu ou gèrent un certain type de données. Pour plus d’informations, consultez la [liste des interfaces de diffusion multimédia en continu](list-of-multimedia-streaming-interfaces.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de l’architecture de diffusion multimédia en continu](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



