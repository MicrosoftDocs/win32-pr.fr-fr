---
title: Installation à partir du Web en ligne
description: Installation à partir du Web en ligne
ms.assetid: 891483b0-6ba4-4ed4-b043-c6c109dc696b
keywords:
- Windows Media Player Online stores, installation à partir du Web en ligne
- magasins en ligne, installation à partir du Web en ligne
- tapez 1 magasins en ligne, installation à partir du Web en ligne
- tapez 2 magasins en ligne, installation à partir du Web en ligne
- Windows Media Player Online stores, en ligne installe à partir du Web
- magasins en ligne, installations en ligne à partir du Web
- tapez 1 magasins en ligne, installations en ligne à partir du Web
- tapez 2 magasins en ligne, installations en ligne à partir du Web
- installation de magasins en ligne à partir du Web en ligne
- installations en ligne de magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd342d3fc79cf3012d5bc290561a9b63167e044f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106540746"
---
# <a name="installing-from-the-web-while-online"></a>Installation à partir du Web en ligne

Les utilisateurs peuvent installer le lecteur Windows Media en tant que téléchargement Web tout en étant connecté à Internet. Dans ce cas, Microsoft peut configurer le magasin en ligne initial que vous spécifiez.

Pour redistribuer le lecteur Windows Media de cette manière, utilisez l’URL suivante :

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*version*&UserLocale =*localID*&service =*clé*

Dans l’URL précédente, définissez *Key* sur le nom de clé de votre magasin en ligne et définissez *LocaleID* sur l’identificateur des paramètres régionaux dans lesquels votre magasin fournit le service. Définissez la *version* sur 2 pour le lecteur Windows Media 11 sur Windows XP ou 1 pour le lecteur Windows Media 10. L’URL installe le lecteur Windows Media et définit le magasin actif initial sur celui spécifié par la *clé*.

L’exemple suivant montre une URL qui installe le lecteur Windows Media 11 et définit Proseware comme magasin actif initial. La valeur de 409 pour *LocaleID* indique que Proseware fournit le service dans le États-Unis.

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=2&UserLocale=409&Service=Proseware

Si le document ServiceInfo du magasin en ligne comprend un élément installer, le programme d’installation du lecteur Windows Media personnalisera le processus d’installation. À l’aide des valeurs d’attribut, le programme d’installation affiche votre contrat de licence utilisateur final (CLUF) et votre déclaration de confidentialité, et récupère et installe également votre fichier. cab sur l’ordinateur de l’utilisateur. Par exemple, vous pouvez utiliser cette fonctionnalité pour installer la dernière version d’un objet COM requis par votre magasin en ligne.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Élément d’installation**](install-element.md)
</dt> <dt>

[**Document ServiceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Définition de la boutique en ligne initiale**](setting-the-initial-online-store.md)
</dt> </dl>

 

 




