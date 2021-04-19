---
description: Il est généralement préférable de copier un ensemble d’informations plus complexe que ce qui peut être contenu dans le format ISF (Ink Serialized Format).
ms.assetid: 1cef7f91-118c-4a16-802d-bd2ec5d15416
title: Stockage de l’encre en HTML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8372e6e77ea0284bc44fa70883964e53b3063bab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544999"
---
# <a name="storing-ink-in-html"></a>Stockage de l’encre en HTML

Il est généralement préférable de copier un ensemble d’informations plus complexe que ce qui peut être contenu dans le format ISF (Ink Serialized Format). Le format HTML est particulièrement utile en tant que format d’interopérabilité en raison de son acceptation forte comme une norme industrielle et de sa capacité à représenter du contenu hétérogène.

Le langage HTML est largement compréhensible, bien documenté et familier à de nombreux développeurs. Il existe de nombreux outils pour la production HTML. En outre, Microsoft Windows contient des API (Application Programming Interfaces) pour le rendu et la manipulation du code HTML. Enfin, les API de la plate-forme Tablet PC fournissent le format de persistance GIF renforcé, qui convient pour l’incorporation dans d’autres formats, plus important en HTML. Ce format est constitué d’un fichier GIF avec Ink Serialized Format (ISF) incorporé dans un bloc d’extension d’application.

Ces fichiers GIF sont des représentations d’objets Ink qui :

-   Rendu dans les applications qui ne sont pas compatibles avec l’encre, telles que les navigateurs ou les traitements de texte hérités.
-   Contiennent toutes les informations nécessaires à partir de l’encre d’origine qu’il convient de conserver à des fins telles que la modification ou la reconnaissance.

Ces fichiers GIF peuvent être générés à l’aide des méthodes de persistance des API de la plateforme Tablet PC. Il s’agit de gif et doit utiliser l’extension GIF et, pour une application qui n’est pas compatible avec l’écriture manuscrite, il n’y a rien de différent à partir d’un GIF normal. Toutefois, dans une application compatible avec l’écriture manuscrite, il existe un ensemble complet de données sous-jacentes de l’image.

Une fois produit par les API de la plateforme Tablet PC, un fichier GIF viné est référencé par une balise IMG en HTML. Le code HTML est ensuite stocké dans l' \_ emplacement du presse-papiers html CF standard. Cela permet d’afficher le code HTML pour d’autres applications, qu’elles soient compatibles avec l’encre. L’image elle-même peut être stockée dans le cache Windows Internet et définie pour un âge après un laps de temps approprié.

Des ornements spécifiques à la balise IMG sont fournis ou requis. Ces ornements identifient le code HTML comme contenant de l’encre. L’exemple suivant fait référence à une image GIF supplémentée à l’aide de balises HTML :

`<img href="34372423432.gif" />`

S’il est nécessaire de faire référence à l’image par d’autres moyens, tels que des feuilles de style en cascade ou des langage VML (VML), il doit toujours y avoir une balise IMG référençant l’image. Cela permet de couper-coller dans et hors des applications qui acceptent les représentations HTML d’encre.

Les applications qui prennent en charge l’écriture manuscrite en HTML doivent :

-   Générez \_ le code html CF lorsque l’utilisateur exécute une copie. Lors de la génération du \_ code html CF sur Copy (ou Save As html), utilisez la méthode [Microsoft. Ink. Ink. Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) , en spécifiant la valeur [Microsoft. Ink. PersistenceFormat](/previous-versions/ms827245(v=msdn.10)) dans le paramètre *p* , afin de générer une image gif supplémentée. Le texte de remplacement doit être défini sur le résultat de reconnaissance le plus précis. Vous pouvez définir un positionnement absolu ou sur place, selon vos besoins.
-   Vérifiez toutes les balises IMG pour déterminer si les images qu’elles pointent contiennent de l’encre, si l' \_ emplacement html CF est choisi pour un collage. Dans ce cas, traite les images en tant qu’objets [Ink](/previous-versions/aa515768(v=msdn.10)) en interne. Bien que seuls les fichiers GIF soient pris en charge dans cette version, votre application doit également vérifier les images non GIF, au cas où des formats d’image supplémentaires seront pris en charge à l’avenir.
-   Prendre en charge la copie et le collage de ISF. Les applications qui prennent en charge HTML doivent également prendre en charge ISF pour améliorer l’interopérabilité avec les applications compatibles avec l’encre qui ne reconnaissent pas le format HTML. Cela est similaire à la Convention selon laquelle les applications qui placent du code HTML dans le presse-papiers placent également le texte.

Pour plus d’informations sur les gif enrichis, consultez [blocs de construction](building-blocks.md).

 

 
