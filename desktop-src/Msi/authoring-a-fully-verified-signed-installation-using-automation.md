---
description: L’exemple suivant montre comment remplir la table MsiDigitalCertificate et la table MsiDigitalSignature à l’aide d’une sous-routine Visual Basic pour Applications (VBA).
ms.assetid: 3a23a721-0672-4eac-bdf2-434282b92590
title: Création d’une installation signée entièrement vérifiée à l’aide d’Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99267feffac71401f36635c08fa7f9f6598a0c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951766"
---
# <a name="authoring-a-fully-verified-signed-installation-using-automation"></a><span data-ttu-id="36b9d-103">Création d’une installation signée entièrement vérifiée à l’aide d’Automation</span><span class="sxs-lookup"><span data-stu-id="36b9d-103">Authoring a Fully Verified Signed Installation Using Automation</span></span>

<span data-ttu-id="36b9d-104">L’exemple suivant montre comment remplir la table [MsiDigitalCertificate](msidigitalcertificate-table.md) et la [table MsiDigitalSignature](msidigitalsignature-table.md) à l’aide d’une sous-routine Visual Basic pour applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="36b9d-104">The following sample demonstrates how to populate the [MsiDigitalCertificate table](msidigitalcertificate-table.md) and [MsiDigitalSignature table](msidigitalsignature-table.md) by using a Visual Basic for Applications (VBA) subroutine.</span></span> <span data-ttu-id="36b9d-105">Pour plus d’informations sur la sécurisation des packages Windows Installer, consultez [instructions pour la création d’installations sécurisées](guidelines-for-authoring-secure-installations.md).</span><span class="sxs-lookup"><span data-stu-id="36b9d-105">For more information about securing Windows Installer packages see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md).</span></span>

<span data-ttu-id="36b9d-106">La [**méthode FileSignatureInfo**](installer-filesignatureinfo.md) retourne un SAFEARRAY d’octets.</span><span class="sxs-lookup"><span data-stu-id="36b9d-106">The [**FileSignatureInfo method**](installer-filesignatureinfo.md) returns a SAFEARRAY of bytes.</span></span> <span data-ttu-id="36b9d-107">Pour plus d’informations, consultez [**type de données SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="36b9d-107">For more information, see the [**SAFEARRAY Data Type**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span> <span data-ttu-id="36b9d-108">Les données de ce tableau doivent être converties au format Unicode, car Visual Basic ne dispose pas d’un moyen d’écrire des octets directement dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="36b9d-108">The data from this array must be converted to Unicode because Visual Basic does not have a way to write bytes straight into a file.</span></span> <span data-ttu-id="36b9d-109">La [**méthode SetStream**](record-setstream.md) peut ensuite utiliser le fichier de données converties pour écrire des données de flux dans un champ d’enregistrement spécifié d’un [**objet enregistrement**](record-object.md).</span><span class="sxs-lookup"><span data-stu-id="36b9d-109">The [**SetStream method**](record-setstream.md) can then use the file of converted data to write stream data into a specified record field of a [**Record object**](record-object.md).</span></span> <span data-ttu-id="36b9d-110">Notez que la conversion des données d’octets en Unicode peut potentiellement modifier les données et que les données converties doivent correspondre aux données d’origine pour une vérification de signature correcte.</span><span class="sxs-lookup"><span data-stu-id="36b9d-110">Note that conversion of the byte data to Unicode can potentially change the data and that the converted data must match the original data for correct signature verification.</span></span> <span data-ttu-id="36b9d-111">L’auteur du package doit s’assurer que les données d’origine et de conversion correspondent.</span><span class="sxs-lookup"><span data-stu-id="36b9d-111">The package author must ensure that the original and converted data match.</span></span>


```VB
Sub PopulateDigitalSignature()

    Dim Installer As Object
    Dim Database As Object
    Dim x() As Byte
    
    Const szSignedCabinet = "c:\test.cab"
    Const szCertFile = "c:\temp\test.cer"
    Const szDatabase = "c:\test.msi"
        
    Set Installer = CreateObject("WindowsInstaller.Installer")
    
    x = Installer.FileSignatureInfo(szSignedCabinet, 0, msiSignatureInfoCertificate)
    
    Dim fs, ts
    Dim s As String
    Set fs = CreateObject("Scripting.FileSystemObject")
    Set ts = fs.CreateTextFile(szCertFile, True)        'Create a file
    
    s = StrConv(x, vbUnicode)
    ts.Write s
    ts.Close
        
    Set Database = Installer.OpenDatabase(szDatabase, msiOpenDatabaseModeTransact)
    Set ViewCert = Database.OpenView("SELECT * FROM `MsiDigitalCertificate`")
    ViewCert.Execute 0
    Set ViewSig = Database.OpenView("SELECT * FROM `MsiDigitalSignature`")
    ViewSig.Execute 0
    
    Set RecordCert = Installer.CreateRecord(2)
    RecordCert.StringData(1) = "Test"
    RecordCert.SetStream 2, szCertFile
    ViewCert.Modify msiViewModifyInsert, RecordCert
    
    Set RecordSig = Installer.CreateRecord(4)
    RecordSig.StringData(1) = "Media"
    RecordSig.StringData(2) = "1"
    RecordSig.StringData(3) = "Test"
    ViewSig.Modify msiViewModifyInsert, RecordSig
    
    Database.Commit
      fs.DeleteFile(szCertFile)
End Sub
```



 

 
