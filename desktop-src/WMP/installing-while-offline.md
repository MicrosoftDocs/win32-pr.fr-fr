---
title: Installation en mode hors connexion
description: Installation en mode hors connexion
ms.assetid: 29d80b6b-161d-44a7-b91e-70766b849c55
keywords:
- Lecteur Windows Media des magasins en ligne, installation en mode hors connexion
- magasins en ligne, installation en mode hors connexion
- tapez 1 magasins en ligne, installation en mode hors connexion
- tapez 2 magasins en ligne, installation en mode hors connexion
- Lecteur Windows Media les magasins en ligne, installations hors connexion
- magasins en ligne, installations hors connexion
- types 1 magasins en ligne, installations hors connexion
- type 2 magasins en ligne, installations hors connexion
- installation de magasins en ligne en mode hors connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3051aca9634bc2c53950baa783bcf62fc6861c616facd9dc563d70d011c2459
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135502"
---
# <a name="installing-while-offline"></a>Installation en mode hors connexion

les utilisateurs peuvent installer Lecteur Windows Media alors qu’ils ne sont pas connectés à Internet. dans ce cas, Lecteur Windows Media installation localise le document ServiceInfo.xml spécifié par le paramètre de ligne de commande *ServiceInfo* . si l’attribut de **clé** correspond au paramètre de ligne de commande *DefaultService* , le programme d’installation applique les informations des éléments suivants à Lecteur Windows Media :

-   Convivial. le nom convivial du magasin en ligne est affiché dans l’interface utilisateur Lecteur Windows Media.
-   Couleur. Les couleurs spécifiées sont appliquées à la barre des tâches et aux boutons.
-   ServiceTask1, ServiceTask2 et ServiceTask3. Les éléments enfants ButtonText et ButtonTip sont définis. L’attribut URL n’est pas défini. l’URL est définie une fois que l’utilisateur se connecte à Internet et Lecteur Windows Media récupère la liste des magasins en ligne de manière normale.
-   Image. Les attributs MenuURL et ServiceLargeURL sont définis. Ces URL doivent pointer vers les images que vous avez installées sur le disque dur de l’utilisateur à l’aide du protocole file://.

lorsque l’utilisateur tente d’afficher le magasin en ligne, Lecteur Windows Media affiche un message informant l’utilisateur qu’une connexion Internet est requise.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Color, élément**](color-element.md)
</dt> <dt>

[**FriendlyName, élément**](friendlyname-element.md)
</dt> <dt>

[**Élément Image**](image-element.md)
</dt> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Élément ServiceInfo**](serviceinfo-element.md)
</dt> <dt>

[**Élément ServiceTask1**](servicetask1-element.md)
</dt> <dt>

[**Élément ServiceTask2**](servicetask2-element.md)
</dt> <dt>

[**Élément ServiceTask3**](servicetask3-element.md)
</dt> <dt>

[**Définition de la boutique en ligne initiale**](setting-the-initial-online-store.md)
</dt> <dt>

[**Paramètres de ligne de commande d’installation pour les magasins en ligne**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




