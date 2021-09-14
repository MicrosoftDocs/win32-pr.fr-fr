---
description: Les certificats peuvent être ajoutés ou supprimés des magasins de certificats si le magasin est ouvert avec l’autorisation de lecture/écriture.
ms.assetid: a1cb6e1e-0702-4f73-827e-3f9e9237b4b6
title: Ajout de certificats à un magasin de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6f4c018be697f48e40d52480f49694762fb956f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123277"
---
# <a name="adding-certificates-to-a-certificate-store"></a>Ajout de certificats à un magasin de certificats

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP. utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité. Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]

Les [*certificats*](../secgloss/c-gly.md) peuvent être ajoutés ou supprimés des [*magasins de certificats*](../secgloss/c-gly.md) si le magasin est ouvert avec l’autorisation de lecture/écriture. L’autorisation de lecture/écriture n’est pas accordée aux magasins de Active Directory. Alors que les certificats peuvent être ajoutés ou supprimés des magasins de mémoire, les modifications apportées aux magasins de mémoire ne sont pas conservées entre les sessions.

Les certificats peuvent être ajoutés à un magasin de certificats ouvert avec l’autorisation de lecture/écriture à l’aide de la méthode **Add** . Un certificat peut être supprimé d’un magasin de certificats ouvert avec l’autorisation de lecture/écriture à l’aide de la méthode **Remove** . Vous pouvez créer et enregistrer de nouveaux magasins dans le magasin de l’utilisateur actuel CAPICOM et dans les emplacements du magasin de l' \_ \_ \_ \_ ordinateur local CAPICOM \_ \_ . Les magasins nouvellement créés dans l’un de ces emplacements peuvent être ouverts avec l’autorisation de lecture/écriture.

Dans l’exemple suivant, deux magasins de certificats sont ouverts. Les certificats des objets dont le nom commence par F sont récupérés à partir du magasin de Active Directory. Le magasin de l' \_ utilisateur actuel CAPICOM \_ \_ , CAPICOM ca Store \_ Store \_ est ensuite ouvert en tant que magasin de lecture/écriture et le premier certificat de la collection de certificats dans le magasin de Active Directory est ajouté aux certificats dans le \_ magasin d’autorités de certification CAPICOM \_ .

À des fins de démonstration, l’exemple montre l’ouverture des magasins dans le magasin de mémoire CAPICOM, le magasin de l' \_ \_ \_ utilisateur actuel CAPICOM \_ et l' \_ emplacement du \_ magasin local de l’ordinateur local CAPICOM \_ \_ . L’exemple montre l’exportation de tous les certificats à partir d’un magasin ouvert, l’écriture des certificats exportés dans un fichier, leur lecture et leur importation dans un autre magasin. Les certificats que vous venez d’importer sont énumérés et affichés.

Sur toute erreur CAPICOM, une valeur décimale négative de **Err. Number** est retournée. Pour plus d’informations, consultez [**code d' \_ erreur \_ CAPICOM**](capicom-error-code.md). Pour plus d’informations sur les valeurs décimales positives de **Err. Number**, consultez winerror. h.

L’exemple suivant illustre l’ouverture de magasins de certificats à l’aide d’une liaison précoce dans la déclaration des objets de **magasin** et la création d’une instance de ces objets.


```VB
Sub AddCert()
On Error GoTo ErrorHandler
' The following shows two different ways to declare and
' create a store object.

Dim myADstore As New Store

Dim myCAstore As Store
Set myCAstore = New Store

' In this example, the Active Directory store will be searched for a 
' certificate with a subject name that begins with the letter F. 
' This is done by using the string "SN=F*" as the name of the store.

Dim SubjectNameSN As String
SubjectNameSN = "SN=F*"

' Active Directory stores can only be opened with read-only
' access.

myADstore.Open CAPICOM_ACTIVE_DIRECTORY_USER_STORE,
                SubjectNameSN , CAPICOM_STORE_OPEN_READ_ONLY

'  This example assumes that the store opened and that
'  at least one certificate was returned.
'  A complete application would ensure that at least one certificate
'  was in the store before proceeding and would
'  also select one or more of the certificates returned
'  to be added instead of using the first certificate
'  in the collection.

'  Open the MY store so that a certificate can be added.

myCAstore.Open CAPICOM_CURRENT_USER_STORE, CAPICOM_MY_STORE,
                    CAPICOM_STORE_OPEN_READ_WRITE

myCAstore.Add myADstore.certificates.Item(1)

' Release the two store objects.

Set myCAstore = Nothing
Set myADstore = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub


```



 

 
