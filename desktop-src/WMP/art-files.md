---
title: Fichiers art
description: Fichiers art
ms.assetid: 93893610-de8d-4b9a-b23d-75ddb3e1e557
keywords:
- habillages Lecteur Windows Media, fichiers artistiques
- apparences, fichiers artistiques
- fichiers pour les habillages, illustrations
- fichiers art pour les habillages, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89ccf07757e511f7717cbe3bbeff2cdacee004da8d3b64d27ddcef7ae2199a29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956369"
---
# <a name="art-files"></a>Fichiers art

Vous devez créer un ou plusieurs fichiers artistiques pour votre apparence. Sans art, l’utilisateur n’aura rien à regarder. Vous pouvez créer une apparence invisible, mais personne ne l’affichera ! Et même dans ce cas, vous devez toujours créer des fichiers art pour contenir vos images invisibles, car le fichier de définition d’apparence requiert des fichiers artistiques pour des éléments spécifiques.

Il existe trois utilisations de l’art dans les habillages : images principales, images de mappage et autres images.

## <a name="primary-images"></a>Images principales

Vous devez créer une image principale pour votre apparence. C’est ce que les utilisateurs verront quand ils installeront votre apparence. L’image principale est composée d’une ou de plusieurs images créées par des contrôles d’apparence spécifiques.

Si vous avez plus d’un contrôle, vous devez spécifier l’ordre de plan, qui définit les contrôles qui sont affichés devant les autres contrôles. Chaque élément d' **affichage** aura une image d’arrière-plan à laquelle vous pouvez ajouter d’autres images d’élément, ce qui vous permet de créer une image composite principale.

Vous pouvez également avoir des images secondaires, telles qu’une barre d’État coulissante, qui ne s’affichent pas lorsque votre apparence s’affiche pour la première fois, mais qui s’affichent lorsque l’utilisateur effectue une action. Celles-ci suivent les mêmes règles que les images principales, car elles sont créées avec un ensemble de contrôles.

## <a name="mapping-images"></a>Mapper des images

l’une des fonctionnalités les plus puissantes de Lecteur Windows Media apparences est que vous pouvez utiliser le mappage d’images pour déclencher des événements pour votre apparence. Les images interactives sont des fichiers qui contiennent des images spéciales. toutefois, les images contenues dans un fichier image map ne sont pas censées être affichées par l’utilisateur, mais elles sont utilisées par Lecteur Windows Media pour agir quand l’utilisateur clique sur votre apparence.

Différents contrôles requièrent différents genres de cartes d’images. Par exemple, si vous colorez une partie d’une image mapper une valeur rouge spécifique et que l’utilisateur clique sur la zone correspondante de votre image principale, un bouton déclenche un événement. La couleur est utilisée pour définir les événements déclenchés par un clic dans une zone particulière de l’apparence.

## <a name="alternate-images"></a>Images de remplacement

Vous pouvez également configurer d’autres images à afficher lorsqu’un utilisateur effectue une opération. Par exemple, vous pouvez créer une image de remplacement d’un bouton qui s’affichera uniquement lorsque la souris pointe sur le bouton. C’est un bon moyen de permettre aux utilisateurs de savoir ce qu’ils peuvent faire et permet également d’obtenir une interface utilisateur hautement détectable. En utilisant avec prudence les info-bulles et les images de survol, vous pouvez créer des interfaces utilisateur inhabituelles qui fournissent aux utilisateurs des commentaires sur les options disponibles.

Les sections suivantes fournissent plus d’informations sur les fichiers artistiques :

-   [Images principales](primary-images.md)
-   [Mapper des images](mapping-images.md)
-   [Images de remplacement](alternate-images.md)
-   [Formats de fichier art](art-file-formats.md)
-   [Exemple d’art simple](simple-art-example.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fichiers d’apparence**](skin-files.md)
</dt> </dl>

 

 




