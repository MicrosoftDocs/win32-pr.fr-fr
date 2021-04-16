---
description: Les certificats peuvent être ajoutés ou supprimés des magasins de certificats si le magasin est ouvert avec l’autorisation de lecture/écriture.
ms.assetid: a1cb6e1e-0702-4f73-827e-3f9e9237b4b6
title: Ajout de certificats à un magasin de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6f4c018be697f48e40d52480f49694762fb956f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529235"
---
# <a name="adding-certificates-to-a-certificate-store"></a><span data-ttu-id="17fb3-103">Ajout de certificats à un magasin de certificats</span><span class="sxs-lookup"><span data-stu-id="17fb3-103">Adding Certificates to a Certificate Store</span></span>

<span data-ttu-id="17fb3-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="17fb3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="17fb3-105">Utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="17fb3-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="17fb3-106">Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]</span><span class="sxs-lookup"><span data-stu-id="17fb3-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="17fb3-107">Les [*certificats*](../secgloss/c-gly.md) peuvent être ajoutés ou supprimés des [*magasins de certificats*](../secgloss/c-gly.md) si le magasin est ouvert avec l’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="17fb3-107">[*Certificates*](../secgloss/c-gly.md) can be added to or removed from [*certificate stores*](../secgloss/c-gly.md) if the store is opened with read/write permission.</span></span> <span data-ttu-id="17fb3-108">L’autorisation de lecture/écriture n’est pas accordée aux magasins de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="17fb3-108">Read/write permission is not granted to Active Directory stores.</span></span> <span data-ttu-id="17fb3-109">Alors que les certificats peuvent être ajoutés ou supprimés des magasins de mémoire, les modifications apportées aux magasins de mémoire ne sont pas conservées entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="17fb3-109">While certificates can be added to or removed from memory stores, changes in memory stores are not persisted between sessions.</span></span>

<span data-ttu-id="17fb3-110">Les certificats peuvent être ajoutés à un magasin de certificats ouvert avec l’autorisation de lecture/écriture à l’aide de la méthode **Add** .</span><span class="sxs-lookup"><span data-stu-id="17fb3-110">Certificates can be added to a certificate store that is opened with read/write permission by using the **Add** method.</span></span> <span data-ttu-id="17fb3-111">Un certificat peut être supprimé d’un magasin de certificats ouvert avec l’autorisation de lecture/écriture à l’aide de la méthode **Remove** .</span><span class="sxs-lookup"><span data-stu-id="17fb3-111">A certificate can be removed from a certificate store that is opened with read/write permission by using the **Remove** method.</span></span> <span data-ttu-id="17fb3-112">Vous pouvez créer et enregistrer de nouveaux magasins dans le magasin de l’utilisateur actuel CAPICOM et dans les emplacements du magasin de l' \_ \_ \_ \_ ordinateur local CAPICOM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="17fb3-112">New stores can be created and saved in the CAPICOM\_CURRENT\_USER\_STORE and CAPICOM\_LOCAL\_MACHINE\_STORE locations.</span></span> <span data-ttu-id="17fb3-113">Les magasins nouvellement créés dans l’un de ces emplacements peuvent être ouverts avec l’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="17fb3-113">Newly created stores in either of these locations can be opened with read/write permission.</span></span>

<span data-ttu-id="17fb3-114">Dans l’exemple suivant, deux magasins de certificats sont ouverts.</span><span class="sxs-lookup"><span data-stu-id="17fb3-114">In the following example, two certificate stores are opened.</span></span> <span data-ttu-id="17fb3-115">Les certificats des objets dont le nom commence par F sont récupérés à partir du magasin de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="17fb3-115">Certificates of subjects with last names beginning with F are retrieved from the Active Directory store.</span></span> <span data-ttu-id="17fb3-116">Le magasin de l' \_ utilisateur actuel CAPICOM \_ \_ , CAPICOM ca Store \_ Store \_ est ensuite ouvert en tant que magasin de lecture/écriture et le premier certificat de la collection de certificats dans le magasin de Active Directory est ajouté aux certificats dans le \_ magasin d’autorités de certification CAPICOM \_ .</span><span class="sxs-lookup"><span data-stu-id="17fb3-116">The CAPICOM\_CURRENT\_USER\_STORE, CAPICOM\_CA\_STORE store is then opened as a read/write store and the first certificate from the collection of certificates in the Active Directory store is added to the certificates in the CAPICOM\_CA\_STORE.</span></span>

<span data-ttu-id="17fb3-117">À des fins de démonstration, l’exemple montre l’ouverture des magasins dans le magasin de mémoire CAPICOM, le magasin de l' \_ \_ \_ utilisateur actuel CAPICOM \_ et l' \_ emplacement du \_ magasin local de l’ordinateur local CAPICOM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="17fb3-117">For demonstration purposes, the example shows the opening of stores in the CAPICOM\_MEMORY\_STORE, CAPICOM\_CURRENT\_USER\_STORE, and CAPICOM\_LOCAL\_MACHINE\_STORE locations.</span></span> <span data-ttu-id="17fb3-118">L’exemple montre l’exportation de tous les certificats à partir d’un magasin ouvert, l’écriture des certificats exportés dans un fichier, leur lecture et leur importation dans un autre magasin.</span><span class="sxs-lookup"><span data-stu-id="17fb3-118">The example shows exporting all certificates from an open store, writing the exported certificates to a file, reading them back in, and importing them into a different store.</span></span> <span data-ttu-id="17fb3-119">Les certificats que vous venez d’importer sont énumérés et affichés.</span><span class="sxs-lookup"><span data-stu-id="17fb3-119">The newly imported certificates are them enumerated and displayed.</span></span>

<span data-ttu-id="17fb3-120">Sur toute erreur CAPICOM, une valeur décimale négative de **Err. Number** est retournée.</span><span class="sxs-lookup"><span data-stu-id="17fb3-120">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="17fb3-121">Pour plus d’informations, consultez [**code d' \_ erreur \_ CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="17fb3-121">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="17fb3-122">Pour plus d’informations sur les valeurs décimales positives de **Err. Number**, consultez winerror. h.</span><span class="sxs-lookup"><span data-stu-id="17fb3-122">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="17fb3-123">L’exemple suivant illustre l’ouverture de magasins de certificats à l’aide d’une liaison précoce dans la déclaration des objets de **magasin** et la création d’une instance de ces objets.</span><span class="sxs-lookup"><span data-stu-id="17fb3-123">The following example shows opening certificate stores using early binding in the declaration of the **Store** objects and in creating an instance of those objects.</span></span>


```VB
Sub AddCert()
On Error GoTo ErrorHandler
' The following shows two different ways to declare and
' create a store object.

Dim myADstore As New Store

Dim myCAstore As Store
Set myCAstore = New Store

' In this example, the Active Directory store will be searched for a 
' certificate with a subject name that begins with the letter F. 
' This is done by using the string "SN=F*" as the name of the store.

Dim SubjectNameSN As String
SubjectNameSN = "SN=F*"

' Active Directory stores can only be opened with read-only
' access.

myADstore.Open CAPICOM_ACTIVE_DIRECTORY_USER_STORE,
                SubjectNameSN , CAPICOM_STORE_OPEN_READ_ONLY

'  This example assumes that the store opened and that
'  at least one certificate was returned.
'  A complete application would ensure that at least one certificate
'  was in the store before proceeding and would
'  also select one or more of the certificates returned
'  to be added instead of using the first certificate
'  in the collection.

'  Open the MY store so that a certificate can be added.

myCAstore.Open CAPICOM_CURRENT_USER_STORE, CAPICOM_MY_STORE,
                    CAPICOM_STORE_OPEN_READ_WRITE

myCAstore.Add myADstore.certificates.Item(1)

' Release the two store objects.

Set myCAstore = Nothing
Set myADstore = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub


```



 

 
