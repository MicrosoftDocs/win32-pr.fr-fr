---
description: Enregistre le certificat dans un fichier.
ms.assetid: 2012b39b-47fd-4071-9752-98bb10954fc0
title: 'ICertificate2 :: Save, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Save
- ICertificate2.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3427feb86c705f5558d083bc39673fdf77553f58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530302"
---
# <a name="icertificate2save-method"></a>ICertificate2 :: Save, méthode

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **Save** enregistre le certificat dans un fichier. Cette méthode a été introduite dans CAPICOM 2,0.

## <a name="syntax"></a>Syntaxe


```VB
Certificate.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal IncludeOption ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom du fichier* \[ dans\]
</dt> <dd>

Chaîne qui contient le nom du fichier de sortie où le certificat sera enregistré.

</dd> <dt>

*Mot de passe* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui contient le mot de passe en [*texte clair*](../secgloss/p-gly.md) pour un fichier de [*clé privée*](../secgloss/p-gly.md) . Le mot de passe peut contenir jusqu’à 32 caractères Unicode, y compris un caractère null de fin. Pour plus d’informations sur la protection du mot de passe, consultez [gestion des mots de passe](../secbp/handling-passwords.md).

</dd> <dt>

*Enregistreras* \[ dans, facultatif\]
</dt> <dd>

Valeur de l’énumération du [**\_ certificat CAPICOM \_ \_ sous forme de \_ type**](capicom-certificate-save-as-type.md) qui spécifie le format du fichier de sortie. La valeur par défaut est le **\_ certificat CAPICOM \_ enregistré \_ comme \_ CER**. Le tableau suivant répertorie les valeurs possibles.



| Value                                                                                                                                                                                                                  | Signification                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_CER"></span><span id="capicom_certificate_save_as_cer"></span><dl> <dt>**\_certificat CAPICOM \_ enregistré \_ comme \_ CER**</dt> </dl> | Le fichier de sortie sera au format de fichier. cer sans aucune clé privée enregistrée.<br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_PFX"></span><span id="capicom_certificate_save_as_pfx"></span><dl> <dt>**\_certificat CAPICOM \_ enregistré \_ en tant que \_ pfx**</dt> </dl> | Le fichier de sortie sera formaté en tant que fichier. pfx (PKCS \# 12) et toutes les clés privées associées qui peuvent être exportées seront également enregistrées.<br/> |



 

</dd> <dt>

*IncludeOption* \[ dans, facultatif\]
</dt> <dd>

La valeur du [**\_ certificat CAPICOM \_ inclut \_**](capicom-certificate-include-option.md) l’énumération d’option qui spécifie le nombre de certificats de la chaîne qui sont enregistrés dans le fichier de sortie. La valeur par défaut est le \_ certificat CAPICOM \_ inclut \_ uniquement l' \_ entité End \_ . Le tableau suivant répertorie les valeurs possibles.



| Value                                                                                                                                                                                                                                                             | Signification                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <dt>**le certificat CAPICOM \_ \_ inclut une \_ chaîne \_ à l’exception \_ de la racine**</dt> </dl> | Enregistre tous les certificats de la chaîne à l’exception de l’entité racine<br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <dt>**le certificat CAPICOM \_ \_ inclut une \_ \_ chaîne entière**</dt> </dl>                    | Enregistre la chaîne de certificats complète<br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <dt>**le certificat CAPICOM \_ \_ inclut \_ uniquement l' \_ entité \_ end**</dt> </dl>       | Enregistre uniquement le certificat d’entité finale<br/>                                     |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode génère un CAPICOM \_ E \_ non \_ autorisé lorsqu’il est fait un script à partir d’une application Web.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
