---
description: Une signature standard est utilisée pour signer un texte et enregistrer ce texte signé dans un fichier. Le texte signé peut également être envoyé sur Internet. Le message signé est au \# format PKCS 7.
ms.assetid: 67a36123-4fce-4d40-83c3-b9668221276b
title: Signature d’un document
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ce1754cdfa1e89c23525474bae880dc2809c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544210"
---
# <a name="signing-a-document"></a><span data-ttu-id="98809-105">Signature d’un document</span><span class="sxs-lookup"><span data-stu-id="98809-105">Signing a Document</span></span>

<span data-ttu-id="98809-106">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="98809-106">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="98809-107">Utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="98809-107">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="98809-108">Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]</span><span class="sxs-lookup"><span data-stu-id="98809-108">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="98809-109">Une signature standard est utilisée pour signer un texte et enregistrer ce texte signé dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="98809-109">A standard use of a signature is to sign a text and save that signed text to a file.</span></span> <span data-ttu-id="98809-110">Le texte signé peut également être envoyé sur Internet.</span><span class="sxs-lookup"><span data-stu-id="98809-110">The signed text could also be sent over the Internet.</span></span> <span data-ttu-id="98809-111">Le message signé est au \# format PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="98809-111">The signed message is in PKCS \#7 format.</span></span>

<span data-ttu-id="98809-112">Dans cet exemple, la signature est créée pour le contenu détaché (lorsque le contenu n’est pas inclus avec la signature).</span><span class="sxs-lookup"><span data-stu-id="98809-112">In this example, the signature is created for detached content (when the content is not included with the signature).</span></span> <span data-ttu-id="98809-113">Une signature détachée serait le plus souvent utilisée si le destinataire de la signature a une copie du texte signé exact.</span><span class="sxs-lookup"><span data-stu-id="98809-113">A detached signature would most often be used if the recipient of the signature has a copy of the exact signed text.</span></span> <span data-ttu-id="98809-114">Dans l’exemple ci-dessous, le message d’origine et la signature détachée sont écrits dans des fichiers distincts.</span><span class="sxs-lookup"><span data-stu-id="98809-114">In the example below, the original message and the detached signature are written to separate files.</span></span>

<span data-ttu-id="98809-115">Sur toute erreur CAPICOM, une valeur décimale négative de **Err. Number** est retournée.</span><span class="sxs-lookup"><span data-stu-id="98809-115">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="98809-116">Pour plus d’informations, consultez [**code d' \_ erreur \_ CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="98809-116">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="98809-117">Pour plus d’informations sur les valeurs décimales positives de **Err. Number**, consultez winerror. h.</span><span class="sxs-lookup"><span data-stu-id="98809-117">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="98809-118">La création d’une signature utilise la [*clé privée*](../secgloss/p-gly.md)du signataire.</span><span class="sxs-lookup"><span data-stu-id="98809-118">Creating a signature uses the signer's [*private key*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="98809-119">Une signature peut être créée uniquement si le certificat du signataire avec une clé privée associée est disponible.</span><span class="sxs-lookup"><span data-stu-id="98809-119">A signature can only be created if the signer's certificate with an associated private key is available.</span></span> <span data-ttu-id="98809-120">Cet exemple de la méthode **Sign** ne spécifie pas de signataire.</span><span class="sxs-lookup"><span data-stu-id="98809-120">This example of the **Sign** method does not specify a signer.</span></span> <span data-ttu-id="98809-121">Si aucun signataire n’est spécifié et qu’aucun certificat dans **CAPICOM \_ My \_ Store** n’a de clé privée associée, la méthode **Sign** échoue.</span><span class="sxs-lookup"><span data-stu-id="98809-121">If a signer is not specified and no certificate in **CAPICOM\_MY\_STORE** has an associated private key, the **Sign** method fails.</span></span> <span data-ttu-id="98809-122">Si un seul certificat dans CAPICOM **\_ My \_ Store** est associé à une clé privée, ce certificat et sa clé privée sont utilisés pour créer la signature.</span><span class="sxs-lookup"><span data-stu-id="98809-122">If one and only one certificate in **CAPICOM\_MY\_STORE** has an associated private key, that certificate and its private key is used to create the signature.</span></span> <span data-ttu-id="98809-123">Si plusieurs certificats dans le magasin **\_ mon \_ magasin mon magasin** possèdent une clé privée associée, une boîte de dialogue s’affiche et l’utilisateur peut choisir le certificat à utiliser pour créer la signature.</span><span class="sxs-lookup"><span data-stu-id="98809-123">If more than one certificate in the **CAPICOM\_MY\_STORE** store has an associated private key, a dialog box appears and the user can choose the certificate to be used to create the signature.</span></span>

<span data-ttu-id="98809-124">Quand une application Web utilise la méthode **Sign** , une invite s’affiche toujours et l’autorisation de l’utilisateur est requise avant la création d’une signature qui utilise la clé privée de ce signataire.</span><span class="sxs-lookup"><span data-stu-id="98809-124">When a web-based application uses the **Sign** method, a prompt is always displayed and the user's permission is required before a signature that uses that signer's private key is created.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="98809-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="98809-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98809-126">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="98809-126">**Store.Open**</span></span>](store-open.md)
</dt> <dt>

[<span data-ttu-id="98809-127">**Signataire. certificat**</span><span class="sxs-lookup"><span data-stu-id="98809-127">**Signer.Certificate**</span></span>](signer-certificate.md)
</dt> <dt>

[<span data-ttu-id="98809-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="98809-128">**Attribute**</span></span>](attribute.md)
</dt> <dt>

[<span data-ttu-id="98809-129">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="98809-129">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
