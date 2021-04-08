---
description: L’exemple suivant illustre les aspects de l’utilisation de l’objet Store. Il montre les magasins d’ouverture dans le magasin de mémoire CAPICOM, le magasin de l' \_ \_ \_ utilisateur actuel CAPICOM \_ \_ et les emplacements des magasins de l' \_ ordinateur local CAPICOM \_ \_ .
ms.assetid: bfb7ff48-1d6b-404f-9dd4-6de1898354b7
title: Utilisation de magasins dans différents emplacements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e22fa4d4eca4748d6c4652a8b33d22a1db492a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753437"
---
# <a name="using-stores-in-different-locations"></a><span data-ttu-id="c5c58-104">Utilisation de magasins dans différents emplacements</span><span class="sxs-lookup"><span data-stu-id="c5c58-104">Using Stores in Different Locations</span></span>

<span data-ttu-id="c5c58-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5c58-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c5c58-106">Utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c5c58-106">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="c5c58-107">Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]</span><span class="sxs-lookup"><span data-stu-id="c5c58-107">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="c5c58-108">L’exemple suivant illustre les aspects de l’utilisation de l’objet [**Store**](store.md) .</span><span class="sxs-lookup"><span data-stu-id="c5c58-108">The following example demonstrates aspects of working with the [**Store**](store.md) object.</span></span> <span data-ttu-id="c5c58-109">Il montre les magasins d’ouverture dans le magasin de mémoire CAPICOM, le magasin de l' \_ \_ \_ utilisateur actuel CAPICOM \_ \_ et les emplacements des magasins de l' \_ ordinateur local CAPICOM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c5c58-109">It shows opening stores in the CAPICOM\_MEMORY\_STORE, CAPICOM\_CURRENT\_USER\_STORE, and CAPICOM\_LOCAL\_MACHINE\_STORE locations.</span></span>

<span data-ttu-id="c5c58-110">L’exemple montre l’exportation de [*certificats*](../secgloss/c-gly.md) à partir d’un [*magasin*](../secgloss/c-gly.md)ouvert, l’écriture des certificats exportés dans un fichier, leur lecture et leur importation dans un autre magasin.</span><span class="sxs-lookup"><span data-stu-id="c5c58-110">The example shows exporting [*certificates*](../secgloss/c-gly.md) from an open [*store*](../secgloss/c-gly.md), writing the exported certificates to a file, reading them back in and importing them into a different store.</span></span> <span data-ttu-id="c5c58-111">Les certificats que vous venez d’importer sont ensuite énumérés et affichés.</span><span class="sxs-lookup"><span data-stu-id="c5c58-111">The newly imported certificates are then enumerated and displayed.</span></span>

<span data-ttu-id="c5c58-112">Sur toute erreur CAPICOM, une valeur décimale négative de **Err. Number** est retournée.</span><span class="sxs-lookup"><span data-stu-id="c5c58-112">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="c5c58-113">Pour plus d’informations, consultez [**code d' \_ erreur \_ CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="c5c58-113">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="c5c58-114">Pour plus d’informations sur les valeurs décimales positives de **Err. Number**, consultez winerror. h.</span><span class="sxs-lookup"><span data-stu-id="c5c58-114">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


```VB
Sub OpenStores()

    On Error GoTo ErrorHandler

    'Open Memory, current user, and local machine stores
    Dim MemoryStore As New Store
    Dim CurrentUserStore As New Store
    Dim LocalMachineStore As New Store
    Dim NumCerts As Integer

    MemoryStore.Open(CAPICOM_MEMORY_STORE, "MemStore", _
        CAPICOM_STORE_OPEN_READ_WRITE)
    CurrentUserStore.Open(CAPICOM_CURRENT_USER_STORE, _
        CAPICOM_MY_STORE, CAPICOM_STORE_OPEN_READ_ONLY)
    LocalMachineStore.Open(CAPICOM_LOCAL_MACHINE_STORE, _
        CAPICOM_CA_STORE, CAPICOM_STORE_OPEN_READ_ONLY)

    ' Check the number of certificates in the stores.
    NumCerts = MemoryStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates in the memory store. ")
    NumCerts = CurrentUserStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates in the current user store. ")
    NumCerts = LocalMachineStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates in the local machine store. ")


    '  Export the certificates in the current user MY store
    '  to a file.
    Dim ExportString As String
    ExportString = CurrentUserStore.Export
Open "Exportcerts.txt" For Output As #1
Write #1, ExportString
Close #1

    ' Read the store the file.
    Dim importString As String
Open "exportcerts.txt" For Input As #2
Input #2, importString
Close #2
    MemoryStore.Import(importString)

    ' Check the number of certificates in the memory store after 
    ' import()
    NumCerts = MemoryStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates now in the memory store. ")

    ' Enumerate the certificates in the memory store and display each
    ' certificate
    Dim i As Long
    For i = 1 To NumCerts
        MemoryStore.Certificates.Item(i).Display()
    Next i

    ' Release the store objects
    MemoryStore = Nothing
    CurrentUserStore = Nothing
    LocalMachineStore = Nothing
    Exit Sub
ErrorHandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found: " & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 
