---
description: Lorsqu’un document signé est reçu, la validité de la signature ou des signatures peut être vérifiée.
ms.assetid: 088915d8-768c-4378-a9dd-9347a428aff9
title: Vérification de la signature d’un document
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2886edcb9629011ddf1a0b5fb45a12a11f0556
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413447"
---
# <a name="verifying-the-signature-on-a-document"></a>Vérification de la signature d’un document

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité. Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]

Lorsqu’un document signé est reçu, la validité de la signature ou des signatures peut être vérifiée. Une signature peut être vérifiée pour :

-   Validité du hachage de la signature
-   Validité du certificat du signataire

Le [*hachage*](../secgloss/h-gly.md) de la signature est déchiffré à l’aide de la [*clé publique*](../secgloss/p-gly.md) du signataire trouvé sur le [*certificat*](../secgloss/c-gly.md)du signataire, incluse dans la signature. Si la signature déchiffrée correspond à un nouveau hachage du document d’origine, la signature a été créée par le propriétaire de la clé privée associée à la clé publique utilisée pour déchiffrer le hachage. En outre, le document sur lequel la signature est basée est garanti ne pas avoir été modifié après la création de la signature.

Le certificat qui a fourni la clé publique et l’identité du signataire peut également être vérifié pour vérifier la validité, y compris si le certificat a été révoqué, si le certificat est obsolète ou si le certificat a été émis par un émetteur de certificat approuvé.

Dans l’exemple suivant, le contenu signé et l’objet **SignedData** sont lus à partir d’un fichier et la signature et la validité du certificat utilisé pour créer la signature sont vérifiées.

> [!Note]  
> Si la signature n’est pas valide au chiffrement ou si le certificat du signataire n’est pas valide, une exception est levée et le programme de vérification doit gérer l’exception. Sur toute erreur CAPICOM, une valeur décimale négative de **Err. Number** est retournée. Pour plus d’informations, consultez [**code d' \_ erreur \_ CAPICOM**](capicom-error-code.md). Pour plus d’informations sur les valeurs décimales positives de **Err. Number**, consultez winerror. h.

 


```VB
Sub VerifySig(ByVal FileToVerify As String, ByVal FileBase As String)
On Error GoTo ErrorHandler

Dim sdContent As String
Dim sdCheck As String
Dim mySD As SignedData
Set mySD = New SignedData

' Open a file and read the signature.
Open FileToVerify For Input As #1
Input #1, sdCheck
Close #1

' Open a file and input the plaintext content that was signed.
Open FileBase For Input As #2
Input #2, sdContent
Close #1

' Set the detached content upon which the signature is based.
mySD.Content = sdContent

' Verify the detached signature.
On Error Resume Next
    mySD.Verify sdCheck, True
If Err.Number <> 0 Then
    MsgBox "Signature verification failed. " & Err.Description
Else
    MsgBox "Verification complete."
End If

' Release the SignedData object.
Set mySD = Nothing

Exit Sub
ErrorHandler:
    If Err.Number > 0 Then
        MsgBox "Visual Basic error found: " & Err.Description
    Else
        MsgBox "CAPICOM error found: " & Hex(Err.Number)
    End If
End Sub

```



 

 
