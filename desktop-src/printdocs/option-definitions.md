---
description: En savoir plus sur les définitions d’options dans le schéma PrintCapabilities. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: e81068db-ab8e-420c-a0be-93bc92f3df6f
title: Définitions d’options
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdc7dddb4840de8bc91c7f9ab127fd31319e5399
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549367"
---
# <a name="option-definitions"></a>Définitions d’options

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Lorsque vous définissez une option, il est important de le faire de façon à ce qu’elle puisse être comparée à d’autres instances d’option contenues dans la même fonctionnalité. La comparaison doit être significative, car l’instance d’option est utilisée pour définir la configuration non seulement du périphérique, mais du travail, indépendamment du périphérique ou de PrintCapabilities qui ont été utilisés pour créer la configuration. Les autres instances d’option dans la fonctionnalité peuvent apparaître dans le même document PrintCapabilities ou dans un autre document PrintCapabilities qui représente un appareil différent, un document PrintCapabilities qui est défini par une autre partie qui travaille indépendamment. Une fois qu’un client a sélectionné la configuration de l’appareil à utiliser pour afficher un travail ou un document, cette configuration est généralement enregistrée, avec la tâche ou le document, sous la forme d’un PrintTicket. Le PrintTicket contient un ensemble d’instances d’option, en général une pour chaque fonctionnalité définie dans le document PrintCapabilities. Les instances d’option doivent être portables et doivent préserver l’intention d’impression, afin que l’intention puisse être communiquée lorsque ce PrintTicket est donné à un appareil différent, même un autre document PrintCapabilities écrit par un autre auteur. Le principal avantage de cette portabilité est que si un autre appareil ne prend pas en charge spécifiquement une option contenue dans le PrintTicket, le pilote de périphérique ou le sous-système est en mesure d’identifier et de sélectionner l’option qui est la plus proche de la fonctionnalité.

L’une des principales fonctions PrintTicket du pilote consiste à identifier l’option d’appareil dans le document PrintCapabilities qui correspond le mieux à une option particulière indiquée dans PrintTicket. Pendant ce processus de notation défini pour le pilote de périphérique ou la correspondance, l’option dans PrintTicket est appelée « option de *référence* », tandis que l’option dans le document PrintCapabilities est appelée « option *candidate* ». La mesure de correspondance générale correspond au nombre d’instances ScoredProperty correspondantes dans les instances de l’option candidate et de référence ; un plus grand nombre de correspondances indique généralement une meilleure conservation de l’intention d’impression. Dans votre processus de notation, vous pouvez choisir d’attribuer un poids plus élevé à certains éléments de ScoredProperty que à d’autres.

Vous pouvez rendre des instances d’option portables en veillant à ce que toutes les instances d’option appartenant à la même fonctionnalité aient un ou plusieurs *éléments ScoredProperty en commun*. Cela signifie qu’il existe un ensemble d’éléments ScoredProperty qui apparaît dans chaque instance d’option (appartenant à la même fonctionnalité). Par exemple, les instances d’option pour la fonctionnalité PageMediaSize peuvent être portables si chaque instance d’option contient des éléments ScoredProperty qui définissent les propriétés PageMediaSize intrinsèques : MediaSizeWidth et MediaSizeHeight. Le pilote de périphérique ou le code de sous-système peut ensuite déterminer la différence entre deux instances d’option en comparant les différences entre ces valeurs ScoredProperty. S’il n’existe aucune option dans le document PrintCapabilities qui correspond exactement à celle du PrintTicket, le pilote de périphérique peut facilement déterminer et sélectionner l’option qui a les dimensions de média correspondant les plus proches.

Deux objets (dans le cas présent, les instances d’option) sont considérés comme ayant des éléments *en commun*, ou équivalents à des *éléments correspondants*, si les trois conditions suivantes sont satisfaites.

1.  Les deux éléments sont du même type d’élément.

2.  Les attributs de nom des deux éléments sont identiques (ou aucun élément ne contient un attribut Name).

3.  La chaîne de parents des éléments comparés, à travers les deux objets pris en considération, doit satisfaire aux conditions 1 et 2.

Par exemple, Imaginez une situation dans laquelle il y a deux instances d’option, où chacune contient une instance ScoredProperty et que chacune de ces instances ScoredProperty contient une instance de propriété. En clair, la première condition est satisfaite (les deux instances de propriété sont du même type) et une partie de la troisième condition est satisfaite (les parents des instances de propriété sont du même type, ScoredProperty et les parents de ces éléments sont les instances d’option, qui sont également du même type). Si les attributs de nom de, respectivement, les instances de propriété, les instances ScoredProperty et les instances d’option sont identiques ou ne sont pas fournis, les deux instances d’option ont des éléments en commun.

Dans ce qui précède, la première étape de la création d’instances d’option consiste à définir un ensemble d’éléments ScoredProperty qui sont présents dans la plupart ou la totalité des instances d’option. Si l’attribut de configuration de votre appareil peut être représenté par une fonctionnalité standard (parmi celles indiquées dans les mots clés du schéma d’impression), notez les éléments ScoredProperty en commun dans les instances d’option standard. Vous devez vous assurer que toutes les nouvelles instances d’option que vous introduisez contiennent également ces éléments ScoredProperty. Vous êtes toujours libre d’ajouter des éléments ScoredProperty supplémentaires en fonction des besoins afin de différencier vos instances d’option des instances d’option standard. Vous pouvez même supprimer un ou plusieurs des éléments ScoredProperty en commun s’il y a une bonne raison, bien que cela réduise la portabilité d’une telle option. Bien entendu, les considérations relatives à la portabilité suggèrent d’utiliser les instances d’option standard non modifiées, sauf s’il existe une différence intrinsèque entre votre option et l’instance d’option standard qui doit être reflétée dans la nouvelle instance d’option.

L’exemple suivant illustre une situation pour laquelle vous souhaiterez peut-être ajouter un élément ScoredProperty à une instance option. Toutes les instances d’option standard pour la fonctionnalité PageMediaSize ont les éléments ScoredProperty MediaSizeWidth et MediaSizeHeight en commun. Supposons que votre appareil puisse prendre en charge l’une des tailles de support de lettre standard en alimentant le papier soit transverse (LongEdgeFirst), soit longitudinalement (ShortEdgeFirst). En supposant que vous ne souhaitiez pas introduire une nouvelle fonctionnalité de direction de flux pour exposer ce degré de liberté, vous pouvez à la place modifier les deux instances de l’option PageMediaSize pour la lettre afin d’incorporer l’orientation du flux papier. Pour ces deux instances d’option de lettre, commencez par l’instance d’option PageMediaSize standard et ajoutez un nouvel élément ScoredProperty pour représenter le FeedDirection. Dans une instance d’option, définissez FeedDirection ScoredProperty sur LongEdgeFirst ; dans l’autre instance de l’option, affectez à FeedDirection la valeur ShortEdgeFirst. Notez que ces nouvelles instances d’option maintiennent leur portabilité. Si l’option représentant la lettre, ShortEdgeFirst est enregistrée dans un PrintTicket et qu’un autre périphérique qui prend en charge uniquement l’option standard de lettre est sélectionné pour le rendu du travail, le code de correspondance des options peut déterminer rapidement que la lettre d’option standard est la meilleure correspondance avec la lettre d’option, ShortEdgeFirst. La raison pour laquelle il s’agit de la meilleure correspondance est que toutes les instances ScoredProperty sont conformes, à l’exception du ScoredProperty FeedDirection, qui n’existe pas dans l’option standard de la lettre.

Vous pouvez également rencontrer des cas où les modifications apportées à l’option modifient tellement la signification du fait que l’option modifiée ne peut plus être considérée comme un cas spécialisé de l’original. Dans ce cas, vous devez modifier le nom de l’option pour refléter la différence entre l’instance d’option modifiée et la valeur non modifiée. Seul l’auteur du document PrintCapabilities pour un appareil particulier peut décider si l’option offerte par l’appareil diffère suffisamment d’une instance d’option standard pour garantir une définition incompatible.

Considérons à présent le cas où votre appareil a un attribut de configuration d’appareil qui ne correspond à aucune des instances de fonctionnalités standard. Dans ce cas, vous ne pouvez pas compter sur les instances d’option standard pour fournir la liste des éléments ScoredProperty en commun. Lorsque vous créez une instance ScoredProperty, votre objectif principal est de différencier chaque option des autres dans la fonctionnalité et de décrire la raison pour laquelle un utilisateur sélectionne une option sur une autre. La ligne de base consiste à caractériser chaque option par un attribut de nom unique, et le ScoredProperty qui contient l’attribut Name devient celui utilisé pour déterminer les éléments en commun.

Une fois qu’un ensemble d’éléments ScoredProperty en commun a été établi, il est facile d’assigner des valeurs appropriées à chaque ScoredProperty pour créer chaque option. Comme dans l’exemple précédent, pour certaines instances d’option, vous devrez peut-être ajouter des instances ScoredProperty supplémentaires ou supprimer certains éléments en commun pour créer une instance d’option appropriée.

Il convient de noter que le schéma d’impression exige que le jeu d’instances ScoredProperty, leurs emplacements et les valeurs assignées à chaque ScoredProperty dans une option restent constants, indépendamment de la configuration. L’ensemble du concept du schéma d’impression repose sur des instances d’option ayant des propriétés fixes, identifiables et ScoredProperty partagées entre plusieurs appareils.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



