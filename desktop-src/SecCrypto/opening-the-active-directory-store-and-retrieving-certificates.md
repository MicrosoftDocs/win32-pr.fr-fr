---
description: Les certificats peuvent être récupérés à partir d’un magasin de Active Directory dans lequel sont stockés les certificats des utilisateurs d’un domaine.
ms.assetid: 5c4d1629-88f3-41f4-afb3-7791cd590e6c
title: Ouverture du magasin de Active Directory et récupération des certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd60c7414aaec8b069817b47fbd2493bb11d98c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535479"
---
# <a name="opening-the-active-directory-store-and-retrieving-certificates"></a><span data-ttu-id="ef66f-103">Ouverture du magasin de Active Directory et récupération des certificats</span><span class="sxs-lookup"><span data-stu-id="ef66f-103">Opening the Active Directory Store and Retrieving Certificates</span></span>

<span data-ttu-id="ef66f-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ef66f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ef66f-105">Utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ef66f-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="ef66f-106">Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]</span><span class="sxs-lookup"><span data-stu-id="ef66f-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="ef66f-107">Les [*certificats*](../secgloss/c-gly.md) peuvent être récupérés à partir d’un magasin de Active Directory dans lequel sont stockés les certificats des utilisateurs d’un domaine.</span><span class="sxs-lookup"><span data-stu-id="ef66f-107">[*Certificates*](../secgloss/c-gly.md) can be retrieved from an Active Directory store where the certificates of users of a domain are stored.</span></span> <span data-ttu-id="ef66f-108">Un magasin de Active Directory peut uniquement être ouvert en mode lecture seule et les applications ne peuvent pas ajouter ou supprimer des certificats dans un magasin de Active Directory à l’aide de CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="ef66f-108">An Active Directory store can only be opened in the read-only mode and applications cannot added certificates to or remove certificates from an Active Directory store using CAPICOM.</span></span>

<span data-ttu-id="ef66f-109">Sur toute erreur CAPICOM, une valeur décimale négative de **Err. Number** est retournée.</span><span class="sxs-lookup"><span data-stu-id="ef66f-109">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="ef66f-110">Pour plus d’informations, consultez [**code d' \_ erreur \_ CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="ef66f-110">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="ef66f-111">Pour plus d’informations sur les valeurs décimales positives de **Err. Number**, consultez winerror. h.</span><span class="sxs-lookup"><span data-stu-id="ef66f-111">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="ef66f-112">L’exemple suivant illustre l’ouverture d’un magasin de Active Directory et la récupération de certificats à partir de ce magasin.</span><span class="sxs-lookup"><span data-stu-id="ef66f-112">The following example shows opening an Active Directory store and retrieving certificates from that store.</span></span>


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



 

 
