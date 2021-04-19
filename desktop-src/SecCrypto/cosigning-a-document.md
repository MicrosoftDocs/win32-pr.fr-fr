---
description: Un document peut être signé par plus d’un signataire.
ms.assetid: f81cbf7b-317d-4fab-9b30-88b6c6576db8
title: Cosignature d’un document
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa06cbbc95dc0fe558c6e704bd18102e80221dbc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106530928"
---
# <a name="cosigning-a-document"></a><span data-ttu-id="b00e1-103">Cosignature d’un document</span><span class="sxs-lookup"><span data-stu-id="b00e1-103">Cosigning a Document</span></span>

<span data-ttu-id="b00e1-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b00e1-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b00e1-105">Utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b00e1-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="b00e1-106">Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]</span><span class="sxs-lookup"><span data-stu-id="b00e1-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="b00e1-107">Un document peut être signé par plus d’un signataire.</span><span class="sxs-lookup"><span data-stu-id="b00e1-107">A document can be signed by more than one signer.</span></span> <span data-ttu-id="b00e1-108">Cela se produit quand, par exemple, deux ou plusieurs parties signent un contrat ou une note de frais.</span><span class="sxs-lookup"><span data-stu-id="b00e1-108">This happens when, for instance, two or more parties sign a contract or an expense report.</span></span> <span data-ttu-id="b00e1-109">Dans l’exemple suivant, un document déjà signé est reçu par un deuxième signataire.</span><span class="sxs-lookup"><span data-stu-id="b00e1-109">In the following example, a document already signed is received by a second signer.</span></span> <span data-ttu-id="b00e1-110">Ce signataire utilise la méthode [**cosign**](signeddata-cosign.md) pour attacher une signature supplémentaire au document.</span><span class="sxs-lookup"><span data-stu-id="b00e1-110">This signer uses the [**CoSign**](signeddata-cosign.md) method to attach an additional signature to the document.</span></span>

<span data-ttu-id="b00e1-111">Si une erreur CAPICOM se produit, une valeur négative est retournée dans la propriété **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="b00e1-111">If any CAPICOM error occurs, a negative value is returned in the **Err.Number** property.</span></span> <span data-ttu-id="b00e1-112">Pour plus d’informations sur les codes d’erreur CAPICOM, consultez [**code d' \_ erreur \_ CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="b00e1-112">For more information about CAPICOM error codes, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="b00e1-113">Si le code d’erreur dans la propriété **Err. Number** est une valeur positive, l’erreur est une erreur Windows.</span><span class="sxs-lookup"><span data-stu-id="b00e1-113">If the error code in the **Err.Number** property is a positive value, then the error is a Windows error.</span></span> <span data-ttu-id="b00e1-114">Pour plus d’informations sur les codes d’erreur Windows, consultez winerror. h.</span><span class="sxs-lookup"><span data-stu-id="b00e1-114">For information about Windows error codes, see Winerror.h.</span></span>

> [!Note]
> <span data-ttu-id="b00e1-115">La cosignature d’un document requiert également que le cosignataire dispose d’un [*certificat*](../secgloss/c-gly.md) disponible avec une [*clé privée*](../secgloss/p-gly.md) pour créer la signature.</span><span class="sxs-lookup"><span data-stu-id="b00e1-115">Cosigning a document also requires that the cosigner have an available [*certificate*](../secgloss/c-gly.md) with a [*private key*](../secgloss/p-gly.md) to create the signature.</span></span> <span data-ttu-id="b00e1-116">Si un signataire n’est pas spécifié dans l’appel de la méthode [**Sign**](signeddata-sign.md) et qu’il n’existe pas de certificat dans \_ le \_ magasin mon magasin avec une clé privée associée, la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="b00e1-116">If a signer is not specified in the call of the [**Sign**](signeddata-sign.md) method and there is no certificate in CAPICOM\_MY\_STORE with an associated private key, the method fails.</span></span> <span data-ttu-id="b00e1-117">S’il existe un seul certificat dans CAPICOM \_ My \_ Store avec une clé privée associée, la clé et le certificat sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="b00e1-117">If there is one and only one certificate in CAPICOM\_MY\_STORE with an associated private key, that key and certificate are used.</span></span> <span data-ttu-id="b00e1-118">S’il existe plus d’un certificat utilisable, une invite s’affiche pour permettre à l’utilisateur de choisir le certificat souhaité.</span><span class="sxs-lookup"><span data-stu-id="b00e1-118">If there is more than one usable certificate, a prompt is displayed to allow the user to choose the desired certificate.</span></span>
> 
> <span data-ttu-id="b00e1-119">Si la méthode de [**cosignature**](signeddata-cosign.md) est utilisée dans une application Web, une invite est toujours affichée pour obtenir l’autorisation de l’utilisateur avant la création d’une signature à l’aide de la clé privée de ce signataire.</span><span class="sxs-lookup"><span data-stu-id="b00e1-119">If the [**CoSign**](signeddata-cosign.md) method is used in a web-based application, a prompt is always displayed to get the user's permission before a signature is created by using that signer's private key.</span></span>

 

<span data-ttu-id="b00e1-120">Dans l’exemple suivant, les fichiers qui contiennent le document à signer et les signatures actuelles sur ce document sont lus, la signature est cosignée et la nouvelle signature est écrite dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="b00e1-120">In the following example, files that contain the document to be signed and the current signatures on that document are read, the signature is cosigned, and the new signature is written to a file.</span></span> <span data-ttu-id="b00e1-121">L’exemple utilise une signature détachée avec les données signées et la signature dans des fichiers distincts.</span><span class="sxs-lookup"><span data-stu-id="b00e1-121">The example uses a detached signature with the data signed and the signature in separate files.</span></span>


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



 

 
