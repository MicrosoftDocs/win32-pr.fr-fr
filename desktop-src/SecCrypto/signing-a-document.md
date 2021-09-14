---
description: Une signature standard est utilisée pour signer un texte et enregistrer ce texte signé dans un fichier. Le texte signé peut également être envoyé sur Internet. Le message signé est au \# format PKCS 7.
ms.assetid: 67a36123-4fce-4d40-83c3-b9668221276b
title: Signature d’un document
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ce1754cdfa1e89c23525474bae880dc2809c242
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237444"
---
# <a name="signing-a-document"></a>Signature d’un document

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité. Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]

Une signature standard est utilisée pour signer un texte et enregistrer ce texte signé dans un fichier. Le texte signé peut également être envoyé sur Internet. Le message signé est au \# format PKCS 7.

Dans cet exemple, la signature est créée pour le contenu détaché (lorsque le contenu n’est pas inclus avec la signature). Une signature détachée serait le plus souvent utilisée si le destinataire de la signature a une copie du texte signé exact. Dans l’exemple ci-dessous, le message d’origine et la signature détachée sont écrits dans des fichiers distincts.

Sur toute erreur CAPICOM, une valeur décimale négative de **Err. Number** est retournée. Pour plus d’informations, consultez [**code d' \_ erreur \_ CAPICOM**](capicom-error-code.md). Pour plus d’informations sur les valeurs décimales positives de **Err. Number**, consultez winerror. h.

La création d’une signature utilise la [*clé privée*](../secgloss/p-gly.md)du signataire. Une signature peut être créée uniquement si le certificat du signataire avec une clé privée associée est disponible. Cet exemple de la méthode **Sign** ne spécifie pas de signataire. Si aucun signataire n’est spécifié et qu’aucun certificat dans **CAPICOM \_ My \_ Store** n’a de clé privée associée, la méthode **Sign** échoue. Si un seul certificat dans CAPICOM **\_ My \_ Store** est associé à une clé privée, ce certificat et sa clé privée sont utilisés pour créer la signature. Si plusieurs certificats dans le magasin **\_ mon \_ magasin mon magasin** possèdent une clé privée associée, une boîte de dialogue s’affiche et l’utilisateur peut choisir le certificat à utiliser pour créer la signature.

Quand une application Web utilise la méthode **Sign** , une invite s’affiche toujours et l’autorisation de l’utilisateur est requise avant la création d’une signature qui utilise la clé privée de ce signataire.


```VB
Sub Signfile(ByVal InputFileName As String, _
    ByVal OutputFileName As String)
    
    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim MyStore As New Store
    Dim Signobj As New SignedData
    Dim Signer As New Signer

    ' NOTE: the name 'Attribute' is not a unique name
    ' and must be preceded by 'CAPICOM.'
    Dim SigningTime As New CAPICOM.Attribute

    ' Open the MY store and retrieve the first certificate from the
    ' Store. The signing operation will only work if this
    ' certificate is valid and has access to the signer's private key.
    MyStore.Open CAPICOM_CURRENT_USER_STORE, "MY", _
        CAPICOM_STORE_OPEN_READ_ONLY
    Signer.Certificate = MyStore.Certificates.Item(1)

    ' Open the input file and read the content to be signed from
    ' the file.
    Open App.Path & "\" & InputFileName For Input As #1
    Input #1, c
    Close #1
    
    ' Set the content to be signed.
    Signobj.Content = c

    ' Save the time the data was signed as a signer attribute.
    SigningTime.Name = CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME
    SigningTime.Value = Now
    Signer.AuthenticatedAttributes.Add SigningTime

    ' Sign the content using the signer's private key.
    ' The 'True' parameter indicates that the content signed is not
    ' included in the signature string.
    s = Signobj.Sign(Signer, True)

    Open App.Path & "\" & OutputFileName For Output As #2
    Write #2, s
    Close #2

    MsgBox ("Signature done - Saved to file" & OutputFileName)
    Set Signobj = Nothing
    Set MyStore = Nothing
    Set Signer = Nothing
    Set SigningTime = Nothing

    Exit Sub

ErrorHandler:
    If Err.Number > 0 Then
        MsgBox ("Visual Basic error found:" & Err.Description)
    Else
        MsgBox ("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Store. Open**](store-open.md)
</dt> <dt>

[**Signataire. certificat**](signer-certificate.md)
</dt> <dt>

[**Attribut**](attribute.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
