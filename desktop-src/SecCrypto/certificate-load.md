---
description: Importe un certificat à partir d’un fichier.
ms.assetid: 62c3bf8e-2f52-4342-b3ee-744b032578bf
title: 'ICertificate2 :: Load, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Load
- ICertificate2.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9193297ad7eacc1994e4bf3729a87054573b1574
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537321"
---
# <a name="icertificate2load-method"></a>ICertificate2 :: Load, méthode

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **Load** importe un certificat à partir d’un fichier. Cette méthode a été introduite dans CAPICOM 2,0.

## <a name="syntax"></a>Syntaxe


```VB
Certificate.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ], _
  [ ByVal KeyLocation ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom du fichier* \[ dans\]
</dt> <dd>

Chaîne qui contient le chemin d’accès à un fichier. cer ou. pfx qui contient les données de certificat.

</dd> <dt>

*Mot de passe* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui contient le mot de passe en [*texte clair*](../secgloss/p-gly.md) dans le fichier de [*clé privée*](../secgloss/p-gly.md) . Le mot de passe peut contenir jusqu’à 32 caractères Unicode, y compris un caractère null de fin. Pour plus d’informations sur la protection du mot de passe, consultez [gestion des mots de passe](../secbp/handling-passwords.md).

</dd> <dt>

*KeyStorageFlag* \[ dans, facultatif\]
</dt> <dd>

Valeur de l’énumération de l' [**indicateur de \_ \_ stockage \_ de clé CAPICOM**](capicom-key-storage-flag.md) qui définit les indicateurs de stockage de clé. La valeur par défaut est le \_ \_ stockage par clé CAPICOM \_ par défaut. Le tableau suivant répertorie les valeurs possibles.



| Value                                                                                                                                                                                                                           | Signification                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <dt>**\_ \_ \_ valeur par défaut du stockage de la clé CAPICOM**</dt> </dl>                       | Stockage de clé par défaut.<br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <dt>**\_espace de stockage de clé CAPICOM \_ \_ exportable**</dt> </dl>              | La clé peut être exportée.<br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <dt>**\_clé CAPICOM \_ \_ protégée par l’utilisateur \_**</dt> </dl> | La clé est protégée par l’utilisateur.<br/> |



 

</dd> <dt>

*Emplacement des Keyposition* \[ dans, facultatif\]
</dt> <dd>

Valeur de l’énumération de l' [**\_ \_ emplacement de la clé CAPICOM**](capicom-key-location.md) qui définit les types d’emplacement de clé. La valeur par défaut est la \_ \_ clé utilisateur actuelle CAPICOM \_ . Le tableau suivant répertorie les valeurs possibles.



| Value                                                                                                                                                                                               | Signification                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="CAPICOM_CURRENT_USER_KEY"></span><span id="capicom_current_user_key"></span><dl> <dt>**clé de l' \_ utilisateur actuel CAPICOM \_ \_**</dt> </dl>    | La clé est une clé utilisateur.<br/>    |
| <span id="CAPICOM_LOCAL_MACHINE_KEY"></span><span id="capicom_local_machine_key"></span><dl> <dt>**\_clé d’ordinateur local \_ CAPICOM \_**</dt> </dl> | La clé est une clé d’ordinateur.<br/> |



 

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



 

 
