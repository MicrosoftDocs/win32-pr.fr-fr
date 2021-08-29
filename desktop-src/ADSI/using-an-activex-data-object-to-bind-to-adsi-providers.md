---
title: utilisation d’un objet de données ActiveX pour la liaison aux fournisseurs ADSI
description: étant donné qu’ADSI est également un fournisseur OLE DB, vous pouvez utiliser un objet de données ActiveX (ADO) pour vous connecter aux fournisseurs ADSI.
ms.assetid: b42d804b-f1eb-4085-88aa-015a92309ee8
ms.tgt_platform: multiple
keywords:
- ActiveX de l’objet de données ADSI
- ActiveX de l’objet de données adsi, à l’aide d’ADO pour la liaison aux fournisseurs ADSI
- fournisseurs de services ADSI, à l’aide de ActiveX objet de données à lier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9c34e026fabe34e52bcfbd9182cca935cf7e019b1fd1c3c8f97fd2f88be48c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637529"
---
# <a name="using-an-activex-data-object-to-bind-to-adsi-providers"></a>utilisation d’un objet de données ActiveX pour la liaison aux fournisseurs ADSI

étant donné qu’ADSI est également un fournisseur OLE DB, vous pouvez utiliser un objet de données ActiveX (ADO) pour vous connecter aux fournisseurs ADSI. Comme avec les autres fournisseurs ADO, pour vous connecter à un fournisseur de OLE DB, vous devez créer un objet de connexion et, éventuellement, spécifier les informations d’identification. Le nom du fournisseur d’OLE DB ADSI est **ADSDSOObject**.

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

 

 




