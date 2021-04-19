---
description: La méthode FileSignatureInfo de l’objet installer prend le chemin d’accès à un fichier et retourne un SAFEARRAY d’octets qui représentent le hachage ou le certificat encodé.
ms.assetid: ab34bc46-8a8f-4b48-a1d1-d824ff36a9cc
title: Installer. FileSignatureInfo, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSignatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5dbb758118b7612aaef3f7cca744674bca1c768d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520792"
---
# <a name="installerfilesignatureinfo-method"></a>Installer. FileSignatureInfo, méthode

La méthode **FileSignatureInfo** de l’objet [**installer**](installer-object.md) prend le chemin d’accès à un fichier et retourne un SAFEARRAY d’octets qui représentent le hachage ou le certificat encodé. Les valeurs peuvent ensuite être utilisées pour remplir les tables [MsiDigitalSignature](msidigitalsignature-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)et [MsiDigitalCertificate](msidigitalcertificate-table.md) .

Pour plus d’informations, consultez [**type de données SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).

## <a name="syntax"></a>Syntaxe


```JScript
Installer.FileSignatureInfo(
  FilePath,
  Options,
  Format
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FilePath* 
</dt> <dd>

Chemin d’accès complet à un fichier signé numériquement.

Lors du remplissage des tables [MsiDigitalSignature](msidigitalsignature-table.md) et [MsiDigitalCertificate](msidigitalcertificate-table.md) , *filePath* pointe vers une armoire signée numériquement. Lors du remplissage des tables [MsiPatchCertificate](msipatchcertificate-table.md) et MsiDigitalCertificate, *filePath* pointe vers un correctif signé numériquement.

</dd> <dt>

*Options* 
</dt> <dd>

Indicateurs de cas d’erreur spéciaux.



| Indicateur                                                                                                                                                                                                                                                                                                                                    | Signification                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiSignatureOptionInvalidHashFatal"></span><span id="msisignatureoptioninvalidhashfatal"></span><span id="MSISIGNATUREOPTIONINVALIDHASHFATAL"></span><dl> <dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt> </dl> | Avec les *options* définies sur MsiSignatureOptionInvalidHashFatal, **FileSignatureInfo** retourne toujours une erreur irrécupérable pour un hachage non valide. <br/> Si *options* n’a pas la valeur msiSignatureOptionInvalidHashFatal et que *format* a la valeur msiSignatureInfoCertificate, **FileSignatureInfo** ne retourne pas d’erreur pour un hachage non valide.<br/> |



 

</dd> <dt>

*Format* 
</dt> <dd>

Informations de signature demandées.



| Indicateur                                                                                                                                                                                                                                                                                                        | Signification                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="msiSignatureInfoCertificate"></span><span id="msisignatureinfocertificate"></span><span id="MSISIGNATUREINFOCERTIFICATE"></span><dl> <dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt> </dl> | Retourne un SAFEARRAY d’octets qui représentent le certificat encodé.<br/> |
| <span id="msiSignatureInfoHash"></span><span id="msisignatureinfohash"></span><span id="MSISIGNATUREINFOHASH"></span><dl> <dt>**msiSignatureInfoHash**</dt> <dt>1</dt> </dl>                             | Retourne un SAFEARRAY d’octets qui représentent le hachage.<br/>                |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, la méthode retourne un [SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray) d’octets qui contiennent le hachage ou le certificat encodé.

## <a name="remarks"></a>Notes

Pour créer une installation signée entièrement vérifiée à l’aide de l’automatisation, utilisez la méthode **FileSignatureInfo** pour remplir les tables [MsiDigitalCertificate](msidigitalcertificate-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)et [MsiDigitalSignature](msidigitalsignature-table.md) . Pour plus d’informations, consultez [création d’une installation signée entièrement vérifiée à l’aide d’Automation](authoring-a-fully-verified-signed-installation-using-automation.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Création d’une installation signée entièrement vérifiée à l’aide d’Automation](authoring-a-fully-verified-signed-installation-using-automation.md)
</dt> <dt>

[Signatures numériques et Windows Installer](digital-signatures-and-windows-installer.md)
</dt> <dt>

[**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> </dl>

 

 
