---
title: Création d'une unité d'organisation
description: Maintenant que vous disposez de l’objet domaine, vous pouvez commencer à créer des unités d’organisation.
ms.assetid: c9955b44-5ca1-4b4b-85c8-e0d55a4304ca
ms.tgt_platform: multiple
keywords:
- Création d’une unité d’organisation ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ec0da1efe78d54eba8bc0dc05a998717aaf91f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939599"
---
# <a name="creating-an-organizational-unit"></a>Création d'une unité d'organisation

Maintenant que vous disposez de l’objet domaine, vous pouvez commencer à créer des unités d’organisation. Fabrikam a deux divisions : ventes et production. L’entreprise envisage d’embaucher deux administrateurs Windows 2000 pour gérer chaque division. Joe worden, en tant qu’administrateur d’entreprise, crée deux nouvelles unités d’organisation sous le domaine fabrikam. En créant une unité d’organisation, Joe peut regrouper plusieurs objets et permettre à quelqu’un d’autre de gérer ces objets. L’exemple de code suivant crée l’unité d’organisation Sales (UO).


```VB
Dim dom as IADsContainer
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
Set salesOrg = dom.Create("organizationalUnit", "OU=Sales")
salesOrg.Put "description", "Sales Headquarter,SF"
salesOrg.Put "wwwHomePage", "https://fabrikam.com/sales"
salesOrg.SetInfo
```



La méthode [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) accepte le nom de la classe et le nom du nouvel objet. À ce stade, l’objet n’est pas validé pour Active Directory. Toutefois, vous aurez une référence d’objet ADSI/COM sur le client. Avec cet objet ADSI, vous pouvez définir ou modifier des attributs à l’aide de la méthode [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) . La méthode **IADs. put** accepte le nom d’attribut et la valeur de l’attribut. Toujours, rien n’est validé dans le répertoire ; tout est mis en cache au niveau du client. Quand vous appelez la méthode [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) , les modifications, dans ce cas, la création d’un objet et la modification d’attribut, sont validées dans le répertoire. Ces modifications sont traitées, ce qui signifie que vous verrez soit le nouvel objet avec tous les attributs que vous définissez, soit aucun objet.

Vous pouvez également imbriquer des unités d’organisation. L’exemple de code suivant suppose que la Division Sales est divisée dans les régions est et ouest.


```VB
Set east = salesOrg.Create("organizationalUnit", "OU=East")
east.SetInfo
```



Cela s’applique également à la région ouest.

Pour établir une liaison directe avec la région est de l’organisation Sales, spécifiez le nom unique.


```VB
Set east = GetObject("LDAP://OU=East,OU=Sales,DC=Fabrikam,DC=COM")
Debug.Print east.Get "description"
east.Put "wwwHomePage", "https://fabrikam.com/sales/east"
```



Si vous avez déjà lié l’objet parent (ventes), vous pouvez effectuer une liaison à l’objet enfant (est) à partir de l’objet parent à l’aide du nom relatif de l’objet enfant.


```VB
Set east = salesOU.GetObject("organizationalUnit", "OU=East")
```



Pour vous assurer que les objets ont été créés, utilisez le composant logiciel enfichable MMC utilisateurs et ordinateurs Active Directory pour afficher les nouvelles unités d’organisation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Déplacement des utilisateurs existants vers l’unité d’organisation](moving-existing-users-to-the-organizational-unit.md)
</dt> </dl>

 

 




