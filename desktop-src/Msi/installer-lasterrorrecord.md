---
description: La méthode LastErrorRecord de l’objet installer retourne un objet record qui contient des paramètres d’erreur pour l’erreur la plus récente de la fonction qui a produit l’enregistrement d’erreur.
ms.assetid: 48fe46bc-6c10-4bd5-89bc-013e650a44e6
title: Installer. LastErrorRecord, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.LastErrorRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bb9dad1962cace623a4a52991d3650451a0a6d5f660aad88e46c4fe393ce4e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142108"
---
# <a name="installerlasterrorrecord-method"></a>Installer. LastErrorRecord, méthode

La méthode **LastErrorRecord** de l’objet [**installer**](installer-object.md) retourne un objet [**Record**](record-object.md) qui contient des paramètres d’erreur pour l’erreur la plus récente de la fonction qui a produit l’enregistrement d’erreur.

## <a name="syntax"></a>Syntaxe


```JScript
Installer.LastErrorRecord()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

L’objet [**enregistrement**](record-object.md) est réinitialisé après l’exécution de cette fonction de toute fonction qui génère un enregistrement d’erreur.

Seules les fonctions désignées suivantes génèrent un enregistrement d’erreur :

-   [**OpenDatabase, méthode (objet installer)**](installer-opendatabase.md)
-   [**Commiter**](database-commit.md)
-   [**OpenView**](database-openview.md)
-   [**Port**](database-import.md)
-   [**Exporter**](database-export.md)
-   [**Fusion**](database-merge.md)
-   [**GenerateTransform**](database-generatetransform.md)
-   [**ApplyTransform**](database-applytransform.md)
-   [**Effectue**](view-execute.md)
-   [**Modify**](view-modify.md)
-   [**SetStream**](record-setstream.md)
-   [**SummaryInformation**](database-summaryinformation.md)
-   [**SourcePath**](session-sourcepath.md)
-   [**TargetPath**](session-targetpath.md)
-   [**ComponentCurrentState**](session-componentcurrentstate.md)
-   [**ComponentRequestState**](session-componentrequeststate.md)
-   [**FeatureCurrentState**](session-featurecurrentstate.md)
-   [**FeatureRequestState**](session-featurerequeststate.md)
-   [**FeatureCost**](session-featurecost.md)
-   [**FeatureValidStates**](session-featurevalidstates.md)
-   [**SetInstallLevel**](session-setinstalllevel.md)

L’exemple suivant dans VBScript utilise un appel à [**OpenDatabase**](installer-opendatabase.md) pour montrer comment obtenir des informations d’erreur étendues à partir de l’une des méthodes ou propriétés qui prennent en charge la méthode **LastErrorRecord** . L’exemple construit un message d’erreur lorsque la méthode **OpenDatabase** échoue. L’objet **Err** est utilisé pour déterminer si une erreur a été rencontrée.


```VB
Const msiOpenDatabaseModeReadOnly     = 0

On Error Resume Next ' defer error handling

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' attempt to open the non-existent MSI database
Dim database
Set database = installer.OpenDatabase("c:\nonexistent.msi", msiOpenDatabaseModeReadOnly)

' test for error
If Err.Number <> 0 Then
    Dim message, errorRec
    message = Err.Source & " " & Hex(Err.Number) & ": " & Err.Description
    If Not installer Is Nothing Then
        ' try to obtain extended error info
        Set errorRec = installer.LastErrorRecord
        If Not errorRec Is Nothing Then message = message & vbNewLine & errorRec.FormatText
    End If

    MsgBox message

    ' PLACE ADDITIONAL SCRIPTING CODE HERE TO LOG AND/OR DISPLAY THE MESSAGE AND
    ' DETERMINE WHETHER TO CONTINUE PROCESSING ANYTHING ELSE
End If
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




