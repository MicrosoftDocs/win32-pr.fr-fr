---
description: Lorsqu’un document signé est reçu, la validité de la signature ou des signatures peut être vérifiée.
ms.assetid: 088915d8-768c-4378-a9dd-9347a428aff9
title: Vérification de la signature d’un document
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2886edcb9629011ddf1a0b5fb45a12a11f0556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865450"
---
# <a name="verifying-the-signature-on-a-document"></a><span data-ttu-id="16879-103">Vérification de la signature d’un document</span><span class="sxs-lookup"><span data-stu-id="16879-103">Verifying the Signature on a Document</span></span>

<span data-ttu-id="16879-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="16879-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="16879-105">Utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="16879-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="16879-106">Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]</span><span class="sxs-lookup"><span data-stu-id="16879-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="16879-107">Lorsqu’un document signé est reçu, la validité de la signature ou des signatures peut être vérifiée.</span><span class="sxs-lookup"><span data-stu-id="16879-107">When a signed document is received, the validity of the signature or signatures can be checked.</span></span> <span data-ttu-id="16879-108">Une signature peut être vérifiée pour :</span><span class="sxs-lookup"><span data-stu-id="16879-108">A signature can be checked for:</span></span>

-   <span data-ttu-id="16879-109">Validité du hachage de la signature</span><span class="sxs-lookup"><span data-stu-id="16879-109">Validity of the signature hash</span></span>
-   <span data-ttu-id="16879-110">Validité du certificat du signataire</span><span class="sxs-lookup"><span data-stu-id="16879-110">Validity of the signer's certificate</span></span>

<span data-ttu-id="16879-111">Le [*hachage*](../secgloss/h-gly.md) de la signature est déchiffré à l’aide de la [*clé publique*](../secgloss/p-gly.md) du signataire trouvé sur le [*certificat*](../secgloss/c-gly.md)du signataire, incluse dans la signature.</span><span class="sxs-lookup"><span data-stu-id="16879-111">The signature [*hash*](../secgloss/h-gly.md) is decrypted using the [*public key*](../secgloss/p-gly.md) of the signer found on the signer's [*certificate*](../secgloss/c-gly.md), included as part of the signature.</span></span> <span data-ttu-id="16879-112">Si la signature déchiffrée correspond à un nouveau hachage du document d’origine, la signature a été créée par le propriétaire de la clé privée associée à la clé publique utilisée pour déchiffrer le hachage.</span><span class="sxs-lookup"><span data-stu-id="16879-112">If the decrypted signature matches a new hash of the original document, the signature was created by the owner of the private key associated with the public key used to decrypt the hash.</span></span> <span data-ttu-id="16879-113">En outre, le document sur lequel la signature est basée est garanti ne pas avoir été modifié après la création de la signature.</span><span class="sxs-lookup"><span data-stu-id="16879-113">In addition, the document that the signature is based on is guaranteed not to have been changed after the signature was created.</span></span>

<span data-ttu-id="16879-114">Le certificat qui a fourni la clé publique et l’identité du signataire peut également être vérifié pour vérifier la validité, y compris si le certificat a été révoqué, si le certificat est obsolète ou si le certificat a été émis par un émetteur de certificat approuvé.</span><span class="sxs-lookup"><span data-stu-id="16879-114">The certificate that provided the public key and the identity of the signer can also be checked for validity including such issues as whether the certificate has been revoked, whether the certificate is out of date, or whether the certificate was issued by a trusted certificate issuer.</span></span>

<span data-ttu-id="16879-115">Dans l’exemple suivant, le contenu signé et l’objet **SignedData** sont lus à partir d’un fichier et la signature et la validité du certificat utilisé pour créer la signature sont vérifiées.</span><span class="sxs-lookup"><span data-stu-id="16879-115">In the following example, the content signed and the **SignedData** object are read in from a file and the signature and the validity of the certificate used to create the signature are checked.</span></span>

> [!Note]  
> <span data-ttu-id="16879-116">Si la signature n’est pas valide au chiffrement ou si le certificat du signataire n’est pas valide, une exception est levée et le programme de vérification doit gérer l’exception.</span><span class="sxs-lookup"><span data-stu-id="16879-116">If the signature is not cryptographically valid or the certificate of the signer is not valid, an exception is raised and the verifying program must handle the exception.</span></span> <span data-ttu-id="16879-117">Sur toute erreur CAPICOM, une valeur décimale négative de **Err. Number** est retournée.</span><span class="sxs-lookup"><span data-stu-id="16879-117">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="16879-118">Pour plus d’informations, consultez [**code d' \_ erreur \_ CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="16879-118">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="16879-119">Pour plus d’informations sur les valeurs décimales positives de **Err. Number**, consultez winerror. h.</span><span class="sxs-lookup"><span data-stu-id="16879-119">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

 


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



 

 
