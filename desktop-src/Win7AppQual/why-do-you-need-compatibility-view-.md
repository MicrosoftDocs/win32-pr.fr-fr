---
description: .
ms.assetid: 5B8D3A76-F30B-4F17-9257-0B6ED7F2D753
title: Pourquoi avez-vous besoin d’un affichage de compatibilité ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74fd1902ad77af863e61be36800a8c4f9eabf227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526952"
---
# <a name="why-do-you-need-compatibility-view"></a>Pourquoi avez-vous besoin d’un affichage de compatibilité ?

La fonctionnalité d’affichage de compatibilité suit un ensemble de règles pour afficher correctement le contenu, sans qu’aucune action de l’utilisateur (ou de l’administrateur informatique) ne soit nécessaire dans la mesure du possible. L’affichage de compatibilité permet aux développeurs d’indiquer au navigateur le moteur de rendu à utiliser et permet aux utilisateurs de remplacer les modes de commutation et de choix du navigateur. Si le développeur et le professionnel de l’informatique ne spécifient pas le mode de rendu à utiliser, l’utilisateur voit l’icône « page rompue » à l’extrémité droite de la barre d’adresses, comme le montre l’illustration suivante.

![illustration de l’icône de page cassée à côté de la barre d’adresses](images/iecompatview.png)

Si un utilisateur clique sur l’icône, Windows Internet Explorer 8 bascule les modes de rendu et la page est rechargée instantanément.

Les utilisateurs ne voient pas toujours cette icône. Il s’agit d’une solution secondaire au lieu du mécanisme principal de compatibilité des applications. Windows Internet Explorer affiche cette icône uniquement lorsqu’un changement de l’affichage de compatibilité est pertinent, par exemple quand un utilisateur affiche des pages en mode standard. Dans tous les autres cas, par exemple quand un utilisateur affiche des pages de mode Quirks ou des vues de sites intranet de zone, l’icône n’apparaît pas. Pour plus d’informations sur l’affichage de compatibilité et le moment où l’icône s’affiche, consultez Présentation de l' [affichage de compatibilité](/archive/blogs/ie/).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
