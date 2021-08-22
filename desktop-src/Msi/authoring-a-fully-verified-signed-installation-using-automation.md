---
description: l’exemple suivant montre comment remplir la table MsiDigitalCertificate et la table MsiDigitalSignature à l’aide d’une sous-routine Visual Basic pour Applications (VBA).
ms.assetid: 3a23a721-0672-4eac-bdf2-434282b92590
title: Création d’une installation signée entièrement vérifiée à l’aide d’Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27f1b0b90296ad92e471449213e86721482a545ff1932458b2ad6b21d47b665
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559099"
---
# <a name="authoring-a-fully-verified-signed-installation-using-automation"></a>Création d’une installation signée entièrement vérifiée à l’aide d’Automation

l’exemple suivant montre comment remplir la table [MsiDigitalCertificate](msidigitalcertificate-table.md) et la [table MsiDigitalSignature](msidigitalsignature-table.md) à l’aide d’une sous-routine Visual Basic pour Applications (VBA). pour plus d’informations sur la sécurisation des packages Windows Installer, consultez [instructions pour la création d’Installations sécurisées](guidelines-for-authoring-secure-installations.md).

La [**méthode FileSignatureInfo**](installer-filesignatureinfo.md) retourne un SAFEARRAY d’octets. Pour plus d’informations, consultez [**type de données SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray). les données de ce tableau doivent être converties au format Unicode, car Visual Basic ne dispose pas d’un moyen d’écrire des octets directement dans un fichier. La [**méthode SetStream**](record-setstream.md) peut ensuite utiliser le fichier de données converties pour écrire des données de flux dans un champ d’enregistrement spécifié d’un [**objet enregistrement**](record-object.md). Notez que la conversion des données d’octets en Unicode peut potentiellement modifier les données et que les données converties doivent correspondre aux données d’origine pour une vérification de signature correcte. L’auteur du package doit s’assurer que les données d’origine et de conversion correspondent.


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



 

 
