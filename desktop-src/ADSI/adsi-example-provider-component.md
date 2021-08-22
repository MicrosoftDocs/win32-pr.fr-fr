---
title: Composant fournisseur d’exemples ADSI
description: Les rédacteurs du fournisseur d’interfaces de service Active Directory trouveront cette section particulièrement intéressante, car il décrit en détail le composant fournisseur d’exemples ADSI.
ms.assetid: 1ca73817-7a21-4a39-b496-fc82db26ea4e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f1ff1d998a9db620c6dc6fb4402f126f556c95a45d589410800ea9c4b335a98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023897"
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

 

 




