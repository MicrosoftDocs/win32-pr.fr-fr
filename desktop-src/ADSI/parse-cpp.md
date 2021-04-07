---
title: Analys. COTISATIONS
description: Dans l’exemple de composant fournisseur, un exemple de code de l’analyseur de chemin d’accès du service d’annuaire se trouve dans parse. cpp.
ms.assetid: 5d68065b-0dab-41c9-baf1-f9610656bd6e
ms.tgt_platform: multiple
keywords:
- analyse ADSI parse. cpp
- interface ADSI de l’analyseur de chemin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ee4df5c1c709fde724385fdf5d5cddbafef338
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939583"
---
# <a name="parsecpp"></a>Analys. COTISATIONS

Dans l’exemple de composant fournisseur, un exemple de code de l’analyseur de chemin d’accès du service d’annuaire se trouve dans parse. cpp. L’analyseur de chemin d’accès est un composant clé des composants fournisseurs ADs. Il vérifie la validité syntaxique d’un chemin d’accès ADs passé à ce fournisseur. Si la syntaxe est valide, une structure **OBJECTINFO** est construite, qui contient une version composant de ADspath pour cet objet.

N’oubliez pas qu’il ne s’agit que d’une vérification syntaxique. Au lieu de respecter la casse spéciale pour chaque nouvelle itération du chemin d’accès, toute vérification du chemin d’accès doit être conforme aux règles de grammaire établies par l’analyseur.

Le tableau suivant répertorie les fonctions et les méthodes implémentées dans parse. cpp.



| Élément                      | Description                                                                                                                                                            |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADsObject**             | Analyse l’ADspath qui lui est passé. Cette fonction suit les règles grammaticales suivantes : <ADsObject>  ->  <ProviderName><SampleDSObject><br/>     |
| **SampleDSObject**        | Analyse les règles grammaticales suivantes : <SampleDSObject> -> " \\ \\ " <identifier> " \\ "<Pathname><br/>                                            |
| **ProviderName**          | Ajoute dans le nom du fournisseur, si ce n’est pas le cas.                                                                                                          |
| **PathName**              | Analyse les règles grammaticales suivantes : <Pathname>  ->  <Component> " \\ \\ " <Pathname> ou<br/> <Pathname> -> <Component><br/> |
| **Composant**             | Analyse les règles grammaticales suivantes : <Identifier> ou<br/> <Identifier> "=" <Identifier><br/>                                              |
| **CLexer::CLexer**        | Constructeur standard.                                                                                                                                                  |
| **CLexer :: ~ CLexer**       | Destructeur standard.                                                                                                                                                   |
| **CLexer::GetNextToken**  | Jetons.                                                                                                                                                             |
| **CLexer::NextChar**      | Récupère le caractère unique suivant.                                                                                                                                       |
| **CLexer ::P ushBackToken** | Sauvegarde au début du dernier jeton.                                                                                                                               |
| **CLexer ::P ushbackChar**  | Sauvegarde un caractère.                                                                                                                                                |
| **CLexer::IsKeyword**     | Vérifie la liste de mots clés. Défini dans Globals. h).                                                                                                                          |
| **AddComponent**          | Ajoute ce composant au tableau de composants.                                                                                                                            |
| **AddProviderName**       | Ajoute un nom de fournisseur syntaxiquement correct à la structure **OBJECTINFO** .                                                                                            |
| **AddRootRDN**            | Ajoute le nom RDN (nom unique relatif) de la racine correct à la structure **OBJECTINFO** .                                                            |
| **SetType**               | Définit le type de l’objet.                                                                                                                                           |
| **Type**                  | Analyse le type > « utilisateur » « \| groupe », et ainsi de suite.                                                                                                                          |



 

 

 





