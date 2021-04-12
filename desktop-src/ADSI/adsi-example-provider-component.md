---
title: Composant fournisseur d’exemples ADSI
description: Les rédacteurs du fournisseur d’interfaces de service Active Directory trouveront cette section particulièrement intéressante, car il décrit en détail le composant fournisseur d’exemples ADSI.
ms.assetid: 1ca73817-7a21-4a39-b496-fc82db26ea4e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7bf960021df9a3b26f252584cad2ff3374254a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309266"
---
# <a name="adsi-example-provider-component"></a>Composant fournisseur d’exemples ADSI

Les rédacteurs du fournisseur d’interfaces de service Active Directory trouveront cette section particulièrement intéressante, car il décrit en détail le composant fournisseur d’exemples ADSI. Les rédacteurs de fournisseur ADSI peuvent installer l’exemple de fournisseur et utiliser l’infrastructure de code comme base pour créer leur propre implémentation. Les rubriques suivantes sont présentées :

[Installation du composant de l’exemple de fournisseur](installing-the-example-provider-component.md) décrit comment installer l’exemple de fournisseur ADSI et son répertoire factice. Cette section comprend une liste des paramètres du Registre.

[Définition de répertoire](directory-definition.md) décrit les entrées de répertoire définies par l’exemple de composant fournisseur.

La [gestion de schéma](schema-management.md) décrit la façon dont chaque élément de l’exemple de service d’annuaire de composant fournisseur peut être représenté par un type spécifique d’Active Directory objet.

La [liaison à un objet Active Directory](binding-to-an-active-directory-object.md) décrit comment, étant donné une chaîne ADsPath, l’exemple de composant fournisseur identifie cet élément, crée le type approprié d’Active Directory objet pour celui-ci et récupère le type demandé de pointeur d’interface sur cet objet à retourner au logiciel client ads.

[Objets Enumerator](enumerator-objects.md) répertorie les types spécifiques d’énumérations fournis par le composant de fournisseur d’exemple et le code source dans lequel les implémentations peuvent être trouvées.

La [vue d’ensemble du code](code-overview.md) fournit une description au niveau des tâches de chaque partie de l’exemple de composant fournisseur.

[Détails du code](code-details.md) répertorie les modules logiciels et leur contenu.

 

 




