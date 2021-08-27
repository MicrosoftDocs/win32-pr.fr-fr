---
description: Enregistre les objets de certificat dans la collection.
ms.assetid: 1d4b7bd5-3ed3-4ace-9894-4e89c5cf844f
title: Certificates. Save, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c3d724a6859a1fbc7765822227290facfb2c2f021fce2f5815f32c5e91fe6453
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126759"
---
# <a name="certificatessave-method"></a>Certificates. Save, méthode

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **Save** enregistre les objets de [**certificat**](certificate.md) dans la collection.

## <a name="syntax"></a>Syntaxe


```VB
Certificates.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal ExportFlag ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom du fichier* \[ dans\]
</dt> <dd>

Chaîne qui contient le nom du fichier de sortie dans lequel les certificats seront enregistrés.

</dd> <dt>

*Mot de passe* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui contient le mot de passe en [*texte clair*](../secgloss/p-gly.md) pour un fichier de [*clé privée*](../secgloss/p-gly.md) . La valeur par défaut est la chaîne vide (""). Jusqu’à 32 caractères Unicode, y compris un caractère null de fin, peuvent être utilisés pour le mot de passe. Pour plus d’informations sur la protection du mot de passe, consultez [gestion des mots de passe](../secbp/handling-passwords.md).

</dd> <dt>

*Enregistreras* \[ dans, facultatif\]
</dt> <dd>

Valeur de l’énumération des [**\_ certificats CAPICOM \_ \_ sous forme de \_ type**](capicom-certificates-save-as-type.md) qui spécifie le format du fichier de sortie. La valeur par défaut est CAPICOM \_ certificats \_ Enregistrer \_ comme \_ pfx. Le tableau suivant répertorie les valeurs possibles.



| Value                                                                                                                                                                                                                                          | Signification                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PFX"></span><span id="capicom_certificates_save_as_pfx"></span><dl> <dt>**\_certificats CAPICOM \_ Enregistrer \_ comme \_ pfx**</dt> </dl>                      | Les certificats sont enregistrés en tant que PFX.<br/>      |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PKCS7"></span><span id="capicom_certificates_save_as_pkcs7"></span><dl> <dt>**\_Certificats CAPICOM \_ enregistrés \_ en tant que \_ PKCS7**</dt> </dl>                | Les certificats sont enregistrés sous la forme d’un fichier PKCS \# 7.<br/> |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_SERIALIZED"></span><span id="capicom_certificates_save_as_serialized"></span><dl> <dt>**\_certificats CAPICOM \_ enregistrés \_ sous forme \_ sérialisée**</dt> </dl> | Les certificats sont enregistrés sous forme sérialisée.<br/> |



 

</dd> <dt>

*ExportFlag* \[ dans, facultatif\]
</dt> <dd>

Valeur de l’énumération de l' [**\_ \_ indicateur d’exportation CAPICOM**](capicom-export-flag.md) qui spécifie si les erreurs d’exportation de clé privée sont ignorées. La valeur par défaut est la valeur par défaut d' \_ exportation CAPICOM \_ . Le tableau suivant répertorie les valeurs possibles.



| Value                                                                                                                                                                                                                                                                                          | Signification                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="CAPICOM_EXPORT_DEFAULT"></span><span id="capicom_export_default"></span><dl> <dt>**\_ \_ valeur par défaut d’exportation CAPICOM**</dt> </dl>                                                                                                      | Les erreurs d’exportation de clé privée ne sont pas ignorées.<br/> |
| <span id="CAPICOM_EXPORT_IGNORE_PRIVATE_KEY_NOT_EXPORTABLE_ERROR"></span><span id="capicom_export_ignore_private_key_not_exportable_error"></span><dl> <dt>**\_erreur Impossible d’exporter \_ la \_ \_ clé privée \_ \_ d’exportation \_ CAPICOM**</dt> </dl> | Les erreurs d’exportation de clé privée sont ignorées.<br/>     |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode génère un CAPICOM \_ E \_ non \_ autorisé lorsqu’il est fait un script à partir d’une application Web.

Les objets de [**certificat**](certificate.md) peuvent être récupérés à l’aide de la méthode [**Store. Load**](store-load.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Certificates**](certificates.md)
</dt> </dl>

 

 
