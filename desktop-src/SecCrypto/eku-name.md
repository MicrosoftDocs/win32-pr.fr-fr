---
description: Définit ou récupère une valeur d’énumération qui spécifie le nom CAPICOM de l’utilisation améliorée de la valeur. Il s’agit de la propriété par défaut.
ms.assetid: afce5553-ef18-4a7f-b1c8-fbe00d3277e0
title: 'IEKU :: Name, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.Name
- IEKU.get_Name
- IEKU.put_Name
- EKU.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e0e28a8816d7e4c4f44e3cd1ec0dc479372d66d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416473"
---
# <a name="iekuname-property"></a>IEKU :: Name, propriété

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **Name** définit ou récupère une valeur d’énumération qui spécifie le nom CAPICOM de l’utilisation améliorée de la EKU. Il s’agit de la propriété par défaut.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
EKU.Name As CAPICOM_EKU
```



## <a name="property-value"></a>Valeur de la propriété

Valeur de l’énumération [**\_ EKU de CAPICOM**](capicom-eku.md) qui spécifie le nom CAPICOM de l’utilisation améliorée de la variable. Le tableau suivant répertorie les valeurs possibles.



| Value                                                                                                                                                                                                                           | Signification                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_EKU_OTHER"></span><span id="capicom_eku_other"></span><dl> <dt>**\_autre utilisation améliorée de la EKU \_**</dt> </dl>                                                      | Le certificat utilise le défini dans la stratégie locale. Utilisé si l’utilisation améliorée de la valeur requise n’est pas prédéfinie et que la valeur OID doit être définie par l’application.<br/> |
| <span id="CAPICOM_EKU_SERVER_AUTH"></span><span id="capicom_eku_server_auth"></span><dl> <dt>**authentification du serveur de l' \_ utilisation améliorée de la EKU CAPICOM \_ \_**</dt> </dl>                                   | Le certificat peut être utilisé pour authentifier un serveur.<br/>                                                                                                |
| <span id="CAPICOM_EKU_CLIENT_AUTH"></span><span id="capicom_eku_client_auth"></span><dl> <dt>**authentification du client de l' \_ utilisation améliorée de la EKU CAPICOM \_ \_**</dt> </dl>                                   | Le certificat peut être utilisé pour authentifier un client.<br/>                                                                                                |
| <span id="CAPICOM_EKU_CODE_SIGNING"></span><span id="capicom_eku_code_signing"></span><dl> <dt>**signature du code de l' \_ utilisation améliorée de la \_ \_ connexion**</dt> </dl>                                | Le certificat peut être utilisé pour créer une signature numérique.<br/>                                                                                           |
| <span id="CAPICOM_EKU_EMAIL_PROTECTION"></span><span id="capicom_eku_email_protection"></span><dl> <dt>**\_protection par e-mail de l’utilisation améliorée de la \_ sécurité pour CAPICOM \_**</dt> </dl>                    | Le certificat peut être utilisé pour la protection de la messagerie.<br/>                                                                                                    |
| <span id="CAPICOM_EKU_SMARTCARD_LOGON"></span><span id="capicom_eku_smartcard_logon"></span><dl> <dt>**\_connexion par carte à \_ puce pour CAPICOM \_**</dt> </dl>                       | Le certificat peut être utilisé pour l’ouverture de session par carte à puce. Introduit dans CAPICOM 2,0.<br/>                                                                         |
| <span id="CAPICOM_EKU_ENCRYPTING_FILE_SYSTEM"></span><span id="capicom_eku_encrypting_file_system"></span><dl> <dt>**\_système de fichiers de \_ chiffrement \_ EKU \_ de CAPICOM**</dt> </dl> | Le certificat peut être utilisé pour EFS. Introduit dans CAPICOM 2,0.<br/>                                                                                      |



 

## <a name="remarks"></a>Notes

Lorsque la valeur de cette propriété est réinitialisée, directement ou indirectement, l’intégralité de l' [*État*](../secgloss/s-gly.md) de l’objet est réinitialisée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
