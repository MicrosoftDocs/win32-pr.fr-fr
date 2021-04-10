---
title: Utilisation d’un objet de données ActiveX pour la liaison aux fournisseurs ADSI
description: Étant donné qu’ADSI est également un fournisseur OLE DB, vous pouvez utiliser un objet ADO (ActiveX Data Object) pour vous connecter aux fournisseurs ADSI.
ms.assetid: b42d804b-f1eb-4085-88aa-015a92309ee8
ms.tgt_platform: multiple
keywords:
- ActiveX Data Object ADSI
- ActiveX Data Object ADSI, utilisation d’ADO pour établir une liaison avec des fournisseurs ADSI
- fournisseurs de services ADSI, utilisation de l’objet de données ActiveX pour la liaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4efb64da28d5c4c2596fcf889e3b3db88b77205c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028543"
---
# <a name="using-an-activex-data-object-to-bind-to-adsi-providers"></a>Utilisation d’un objet de données ActiveX pour la liaison aux fournisseurs ADSI

Étant donné qu’ADSI est également un fournisseur OLE DB, vous pouvez utiliser un objet ADO (ActiveX Data Object) pour vous connecter aux fournisseurs ADSI. Comme avec les autres fournisseurs ADO, pour vous connecter à un fournisseur de OLE DB, vous devez créer un objet de connexion et, éventuellement, spécifier les informations d’identification. Le nom du fournisseur d’OLE DB ADSI est **ADSDSOObject**.

Par exemple :


```VB
Dim con As New Connection 
'VBScript use: con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
con.Open "YourDescriptionHere"
```



Dans l’exemple précédent, vous êtes connecté pour le compte de l’utilisateur actuel. Pour spécifier des informations d’identification différentes, utilisez les propriétés de connexion :


```VB
con.Provider = "ADsDSOObject"
con.Properties("User ID") = "jeffsmith"
con.Properties("Password") = "guesswhat?"
con.Properties("Encrypt Password") = True
con.Open "YourDescriptionHere"
```



ADSI OLE DB définit les propriétés de connexion suivantes.



| Propriété           | Type de données   | Default   |
|--------------------|-------------|-----------|
| « ID utilisateur »          | **BSTR**    | **NULL**  |
| « Mot de passe »         | **BSTR**    | **NULL**  |
| « Chiffrer le mot de passe » | **EXPRESSION** | **FALSE** |
| « Indicateur ADSI »        | **Long**    | 0         |



 

En utilisant OLE DB ADO, vous ne pouvez pas lier à un objet spécifique. Toutefois, vous pouvez interroger un objet spécifique et obtenir un jeu de résultats en retour. Seuls les fournisseurs ADSI qui prennent en charge le service [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) bénéficient d’un modèle de programmation ADO.

La propriété indicateur ADSI est utilisée pour spécifier l’option d’authentification de liaison. Cette propriété peut être une combinaison d’indicateurs de l’énumération d’énumération [**\_ d' \_ authentification ADS**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) .

 

 




