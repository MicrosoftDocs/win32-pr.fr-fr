---
description: Un document peut être signé par plus d’un signataire.
ms.assetid: f81cbf7b-317d-4fab-9b30-88b6c6576db8
title: Cosignature d’un document
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa06cbbc95dc0fe558c6e704bd18102e80221dbc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229019"
---
# <a name="cosigning-a-document"></a>Cosignature d’un document

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité. Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]

Un document peut être signé par plus d’un signataire. Cela se produit quand, par exemple, deux ou plusieurs parties signent un contrat ou une note de frais. Dans l’exemple suivant, un document déjà signé est reçu par un deuxième signataire. Ce signataire utilise la méthode [**cosign**](signeddata-cosign.md) pour attacher une signature supplémentaire au document.

Si une erreur CAPICOM se produit, une valeur négative est retournée dans la propriété **Err. Number** . Pour plus d’informations sur les codes d’erreur CAPICOM, consultez [**code d' \_ erreur \_ CAPICOM**](capicom-error-code.md). si le code d’erreur dans la propriété **Err. Number** est une valeur positive, l’erreur est une erreur de Windows. pour plus d’informations sur les codes d’erreur Windows, consultez Winerror. h.

> [!Note]
> La cosignature d’un document requiert également que le cosignataire dispose d’un [*certificat*](../secgloss/c-gly.md) disponible avec une [*clé privée*](../secgloss/p-gly.md) pour créer la signature. Si un signataire n’est pas spécifié dans l’appel de la méthode [**Sign**](signeddata-sign.md) et qu’il n’existe pas de certificat dans \_ le \_ magasin mon magasin avec une clé privée associée, la méthode échoue. S’il existe un seul certificat dans CAPICOM \_ My \_ Store avec une clé privée associée, la clé et le certificat sont utilisés. S’il existe plus d’un certificat utilisable, une invite s’affiche pour permettre à l’utilisateur de choisir le certificat souhaité.
> 
> Si la méthode de [**cosignature**](signeddata-cosign.md) est utilisée dans une application Web, une invite est toujours affichée pour obtenir l’autorisation de l’utilisateur avant la création d’une signature à l’aide de la clé privée de ce signataire.

 

Dans l’exemple suivant, les fichiers qui contiennent le document à signer et les signatures actuelles sur ce document sont lus, la signature est cosignée et la nouvelle signature est écrite dans un fichier. L’exemple utilise une signature détachée avec les données signées et la signature dans des fichiers distincts.


```VB
Sub CoSignContent(ByVal InputFile1Name As String, ByVal _
    InputFile2Name As String, ByVal OutputFileName As String)

    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim CS As String
    Dim Signobj As New SignedData
    Open InputFile1Name for Input as #1
    Input #1, s
    Close #1
    Open InputFileName2 for input as #2
    Input #2, c 
    Close #2

    Signobj.Content = c
    Signobj.Verify(s)
    CS = Signobj.CoSign
    Open OutputFileName for output as #3
    Write #3, CS
    Close # 3
    Signobj = Nothing
    MsgBox("Cosign finished. Cosignature saved to a file.")
    Exit Sub
ErrorHandler:
    If err.number > 0 Then
        MsgBox("Visual Basic error found:" & err.description)
    Else
        MsgBox("CAPICOM error found : " & err.number)
    End If
End Sub
```



 

 
