---
title: entrées, Flux et sorties
description: entrées, Flux et sorties
ms.assetid: f9f979c4-a15c-4f2a-b63c-7fe776394fdd
keywords:
- Windows Media Format SDK, entrées
- Windows Media Format SDK, Streams
- Windows Media Format SDK, sorties
- ASF (Advanced Systems Format), entrées
- ASF (format des systèmes avancés), entrées
- ASF (Advanced Systems Format), flux
- ASF (format de systèmes avancés), flux
- ASF (Advanced Systems Format), sorties
- ASF (format des systèmes avancés), sorties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4518ed60495aa2318ad27cdade2885aa2660698b5dbf2659290dabf985246da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701826"
---
# <a name="inputs-streams-and-outputs"></a>entrées, Flux et sorties

Dans cette documentation, une « entrée » est un flux de données multimédias numériques (audio ou vidéo) que votre application remet à l’objet enregistreur à partir d’une source à l’aide des API appropriées. Les entrées doivent être fournies dans un format pris en charge. Plusieurs formats RVB et YUV standard sont pris en charge comme entrée, et les codecs audio prennent en charge PCM. Si un format d’entrée spécifié n’est pas pris en charge en mode natif par le codec, l’objet Writer instancie un objet d’assistance audio ou Video qui est capable de convertir un grand nombre de formats en formats acceptés par le codec. Pour les entrées audio, l’objet d’assistance ajuste la profondeur de bit, le taux d’échantillonnage et le nombre de canaux si nécessaire. Pour les entrées vidéo, l’objet d’assistance vidéo effectue des conversions d’espace colorimétrique et des ajustements de taille de rectangle. Dans certains cas, des données audio et vidéo compressées peuvent être transmises dans un flux d’entrée. Une entrée peut être d’un autre type de média, en plus des données audio et vidéo, telles que du texte, des commandes de script, des images fixes ou des données de fichiers arbitraires.

Dans cette documentation, une « sortie » fait référence aux données que l’objet lecteur transmet à une application en vue d’un rendu. Une sortie correspond à un flux unique au moment de la lecture. Si vous utilisez l’exclusion mutuelle, tous les flux qui s’excluent mutuellement partagent une sortie unique. En règle générale, les données de sortie se présentent sous la forme de données audio ou vidéo non compressées, bien qu’elles puissent contenir n’importe quel type de données. Les formats de sortie vidéo pris en charge sont répertoriés ailleurs dans cette documentation.

Dans cette documentation, le terme « Stream » fait référence aux données d’un fichier ASF, par opposition à (1) les données de la source d’entrée avant d’être traitées par l’objet Writer, et (2) les données de sortie après qu’elles ont été décompressées par l’objet Reader. Un flux ASF contient des données provenant d’une seule entrée sur l’objet Writer, bien qu’il soit possible de créer plusieurs flux à partir de la même entrée. Un flux a les mêmes paramètres de format et de compression du début à la fin. Un fichier ASF simple a deux flux, un pour l’audio et un pour la vidéo. Un fichier plus complexe peut avoir deux flux audio et plusieurs flux vidéo. Les flux audio peuvent avoir les mêmes paramètres de compression, mais ils contiennent un contenu différent, par exemple une narration dans différentes langues. Les flux vidéo peuvent contenir le même contenu, mais ont des paramètres de compression différents. Le format de média et les paramètres de compression auxquels l’objet enregistreur s’applique à chaque flux sont spécifiés dans le profil.

La relation entre les entrées, les flux et les sorties peut être de trois types de base. Les trois diagrammes suivants illustrent les relations.

Dans la relation la plus basique, qui est un profil sans exclusion mutuelle, chaque entrée est traitée par le writer et insérée dans le fichier ASF sous la forme d’un flux unique. Lors de la lecture, le lecteur lit le flux et fournit des exemples non compressés sous la forme d’une sortie unique, comme indiqué dans le diagramme suivant.

![Diagramme montrant la relation normale entre les entrées, les flux et les sorties.](images/formatsdk03.png)

Une relation plus complexe se produit lorsque l’exclusion mutuelle à vitesse de transmission multiple est utilisée. Dans ce cas, une seule entrée est traitée par le writer et encodée à plusieurs vitesses de transmission. Chaque encodage des données est inséré dans le fichier ASF sous la forme d’un flux distinct. Lors de la lecture, le lecteur détermine le flux à décompresser en fonction de la bande passante disponible. Le lecteur lit ensuite le flux sélectionné et remet les exemples non compressés sous la forme d’une sortie unique, comme indiqué dans le diagramme suivant.

![Diagramme montrant les relations entre les entrées, les flux et les sorties lors de l’utilisation de l’exclusion mutuelle à vitesse de transmission multiple.](images/formatsdk04.png)

Le troisième type de relation peut se produire lorsqu’une exclusion mutuelle basée sur le langage ou personnalisée est utilisée. Dans cette relation, plusieurs entrées sont traitées par le lecteur et sont insérées dans le fichier ASF sous la forme d’un flux individuel. Lors de la lecture, votre application sélectionne manuellement le flux à décompresser en fonction de la logique que vous fournissez. Le lecteur lit ensuite le flux sélectionné et remet les exemples non compressés sous la forme d’une sortie unique. Ce processus peut être utilisé pour inclure des bandes-son dans plusieurs langues. Le diagramme suivant illustre ce processus.

![Diagramme montrant les relations entre les entrées, les flux et les sorties lors de l’utilisation de l’exclusion mutuelle personnalisée.](images/formatsdk02.png)

Il existe une différence dans les relations décrites précédemment. Par exemple, un fichier peut contenir les trois relations, ou une ou deux d’entre elles. Il est également possible de compresser certaines entrées, auquel cas l’enregistreur n’effectue aucune compression supplémentaire. Le lecteur peut également fournir des exemples compressés. Mais quand c’est le cas, vous devez y accéder par numéro de diffusion, et non par numéro de sortie.

> [!Note]  
> les entrées, les vapeurs et les sorties sont des nombres attribués par les objets du kit de développement logiciel (SDK) du Format de média Windows. Flux avoir un numéro de flux, qui est de base 1, que vous définissez dans le profil. Chaque flux est également affecté à un index de flux pour une utilisation dans l’énumération de flux dans un profil. Aucun de ces nombres n’est assuré d’être cohérent entre eux. Autrement dit, le numéro d’entrée 1 peut ne pas correspondre au flux numéro 1, le numéro de flux 1 peut ne pas correspondre à l’index de flux 1, et ainsi de suite.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Concepts**](concepts.md)
</dt> <dt>

[**Exclusion mutuelle**](mutual-exclusion.md)
</dt> </dl>

 

 




