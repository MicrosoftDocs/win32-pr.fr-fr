---
description: Les certificats peuvent être récupérés à partir d’un magasin de Active Directory dans lequel sont stockés les certificats des utilisateurs d’un domaine.
ms.assetid: 5c4d1629-88f3-41f4-afb3-7791cd590e6c
title: Ouverture du magasin de Active Directory et récupération des certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd2dc5810e97669e40b27bc374bee09f16c0a7c9a3b2bd4a1fa2951e1249a737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979120"
---
# <a name="opening-the-active-directory-store-and-retrieving-certificates"></a>Ouverture du magasin de Active Directory et récupération des certificats

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité. Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]

Les [*certificats*](../secgloss/c-gly.md) peuvent être récupérés à partir d’un magasin de Active Directory dans lequel sont stockés les certificats des utilisateurs d’un domaine. Un magasin de Active Directory peut uniquement être ouvert en mode lecture seule et les applications ne peuvent pas ajouter ou supprimer des certificats dans un magasin de Active Directory à l’aide de CAPICOM.

Sur toute erreur CAPICOM, une valeur décimale négative de **Err. Number** est retournée. Pour plus d’informations, consultez [**code d' \_ erreur \_ CAPICOM**](capicom-error-code.md). Pour plus d’informations sur les valeurs décimales positives de **Err. Number**, consultez winerror. h.

L’exemple suivant illustre l’ouverture d’un magasin de Active Directory et la récupération de certificats à partir de ce magasin.


```VB
Sub OpenADStore()
        On Error GoTo ErrorHandler
        Dim mystore As Store
        Set mystore = New Store
        
        ' Put a string that represents the name of a certificate 
        ' subject in SubjectNameCn. In the following example, 
        ' the * wildcard character is used in the string so that
        ' the Active Directory store will be searched for all 
        ' certificates with a subject name beginning with 'S.'
       
        Dim SubjectNameCn As String
        ' The following uses 'cn=' and the * wildcard character.
        ' Using this string, all certificates in the Active Directory
        ' store with a subject name beginning with an 'S' would
        ' be returned.

        SubjectNameCn = "CN=S*"
        
        ' Active Directory stores can only be opened with read-only
        ' access.
        
         mystore.Open CAPICOM_ACTIVE_DIRECTORY_USER_STORE, _
              SubjectNameCn, CAPICOM_STORE_OPEN_READ_ONLY
        
        If mystore.Certificates.Count < 1 Then
               MsgBox "A certificate for " & SubjectNameCn & _
                      " was not found "
        Else
               MsgBox "The certificate has been retrieved."
        End If
        
        Set mystore = Nothing
        Exit Sub

ErrorHandler:
         
         If Err.Number > 0 Then
               MsgBox "Visual Basic error found:" & Err.Description
         Else
               MsgBox "CAPICOM error found : " & Err.Number
         End If
End Sub
```



 

 
