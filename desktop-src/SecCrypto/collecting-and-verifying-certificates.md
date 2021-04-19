---
description: Dans l’exemple qui suit, les certificats dans un magasin local sont énumérés et vérifiés pour la validité.
ms.assetid: 59ae22f6-aa6d-4b53-8a27-73e1e5c62755
title: Collecte et vérification des certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0b160f373d5ade65679fcc4dd87e3c1c86dc4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517615"
---
# <a name="collecting-and-verifying-certificates"></a><span data-ttu-id="899f6-103">Collecte et vérification des certificats</span><span class="sxs-lookup"><span data-stu-id="899f6-103">Collecting and Verifying Certificates</span></span>

<span data-ttu-id="899f6-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="899f6-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="899f6-105">Utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="899f6-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="899f6-106">Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]</span><span class="sxs-lookup"><span data-stu-id="899f6-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="899f6-107">Souvent, un groupe de [*certificats*](../secgloss/c-gly.md) doit être collecté et vérifié.</span><span class="sxs-lookup"><span data-stu-id="899f6-107">Often a group of [*certificates*](../secgloss/c-gly.md) needs to be collected and verified.</span></span> <span data-ttu-id="899f6-108">Cela est souvent fait pour préparer un groupe de destinataires pour un message enveloppé.</span><span class="sxs-lookup"><span data-stu-id="899f6-108">This would often be done to prepare a group of recipients for an enveloped message.</span></span> <span data-ttu-id="899f6-109">Dans l’exemple qui suit, les certificats dans un magasin local sont énumérés et vérifiés pour la validité.</span><span class="sxs-lookup"><span data-stu-id="899f6-109">In the example that follows, the certificates in a local store are enumerated and checked for validity.</span></span> <span data-ttu-id="899f6-110">Ensuite, un magasin de Active Directory est ouvert pour récupérer et ajouter des certificats au magasin local.</span><span class="sxs-lookup"><span data-stu-id="899f6-110">Next, an Active Directory store is opened to retrieve and add to the local store new certificates.</span></span> <span data-ttu-id="899f6-111">La validité des certificats récupérés dans le magasin Active Directory est vérifiée et, s’ils sont valides, ils sont ajoutés au magasin local.</span><span class="sxs-lookup"><span data-stu-id="899f6-111">The certificates retrieved from the active directory store are checked for validity and, if valid, are added to the local store.</span></span> <span data-ttu-id="899f6-112">Les deux magasins sont ensuite fermés.</span><span class="sxs-lookup"><span data-stu-id="899f6-112">Both stores are then closed.</span></span>

<span data-ttu-id="899f6-113">Sur toute erreur CAPICOM, une valeur décimale négative de **Err. Number** est retournée.</span><span class="sxs-lookup"><span data-stu-id="899f6-113">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="899f6-114">Pour plus d’informations, consultez [**code d' \_ erreur \_ CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="899f6-114">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="899f6-115">Pour plus d’informations sur les valeurs décimales positives de **Err. Number**, consultez winerror. h.</span><span class="sxs-lookup"><span data-stu-id="899f6-115">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="899f6-116">Dans cet exemple, le nom du magasin local est passé en tant que paramètre de chaîne.</span><span class="sxs-lookup"><span data-stu-id="899f6-116">In this example, the name of the local store is passed in as a string parameter.</span></span> <span data-ttu-id="899f6-117">Une chaîne indiquant les critères de recherche des certificats dans le magasin de Active Directory est également transmise en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="899f6-117">A string indicating the search criteria for certificates in the Active Directory store is also passed in as a parameter.</span></span>


```VB
Sub CollectValidCerts(ByVal storename As String, ByVal _
    certname As String)

    On Error GoTo errorhandler

    ' Prepare a local certificate store to contain valid
    ' certificates for the recipients of an enveloped
    ' message.

    ' Open the local store and go to the certificates in the store
    '   1. Display the certificate
    '   2. Check the validity of the certificate
    '   3. Remove certificates that are not valid from the store

    Dim LocalStore As New Store
    Dim ADStore As New Store
    Dim i As Long

    LocalStore.Open(CAPICOM_CURRENT_USER_STORE, storename, _
        CAPICOM_STORE_OPEN_READ_WRITE)

    MsgBox("There are " & LocalStore.Certificates.Count & _
        " certificates in this store ")
    For i = 1 To LocalStore.Certificates.Count
        If LocalStore.Certificates.Item(i).IsValid Then
            LocalStore.Certificates.Item(i).Display()
        Else
            MsgBox("A certificate that is not valid was found.")
        End If
    Next i

    ' Open the AD store and retrieve a certificate based
    ' on a string passed into the function. Add any valid
    ' certificates found to the local store.

    ADStore.Open(CAPICOM_ACTIVE_DIRECTORY_USER_STORE, certname, _
        CAPICOM_STORE_OPEN_READ_ONLY)
    MsgBox("There are " & ADStore.Certificates.Count & _
        " certificates in the AD store.")

    For i = 1 To ADStore.Certificates.Count
        If ADStore.Certificates.Item(i).IsValid Then
            ADStore.Certificates.Item(i).Display()
            LocalStore.Add(ADStore.Certificates.Item(i))
        Else
            MsgBox("the certificate from the AD store is not valid.")
        End If
    Next i

    LocalStore = Nothing
    ADStore = Nothing
    MsgBox("Sub finished without error ")
    Exit Sub
errorhandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found:" & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 
