---
description: Permet à une application de transport d’interroger le [*package de sécurité*](../secgloss/s-gly.md) Negotiate pour certains attributs d’un [*contexte de sécurité*](../secgloss/s-gly.md).
ms.assetid: 9e499161-d5fb-4a64-ac36-f82031a3a7c9
title: QueryContextAttributes (Negotiate), fonction (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 8fcc78181a74d048db389455ed5ab145f22ae004cc256e584b634c07b82a0423
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920107"
---
# <a name="querycontextattributes-negotiate-function"></a>QueryContextAttributes (Negotiate) (fonction)

La fonction **QueryContextAttributes (Negotiate)** permet à une application de transport d’interroger le [*package de sécurité*](../secgloss/s-gly.md) Negotiate pour certains [*attributs*](../secgloss/a-gly.md#_security_attribute_gly) d’un [*contexte de sécurité*](../secgloss/s-gly.md).

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS SEC_ENTRY QueryContextAttributes(
  _In_  PCtxtHandle phContext,
  _In_  ULONG       ulAttribute,
  _Out_ PVOID       pBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*phContext* \[ dans\]
</dt> <dd>

Handle vers le [*contexte de sécurité*](../secgloss/s-gly.md) à interroger.

</dd> <dt>

*ulAttribute* \[ dans\]
</dt> <dd>

Spécifie l’attribut du contexte à retourner. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                          | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_ATTR_ACCESS_TOKEN"></span><span id="secpkg_attr_access_token"></span><dl> <dt>**SECPKG \_ \_ \_ Jeton d’accès attr**</dt> <dt>18</dt> </dl>                                       | Le paramètre *pbuffer* contient un pointeur vers une structure [**SecPkgContext \_ AccessToken**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) .<br/> Retourne un handle pour le jeton d’accès.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_AUTHORITY"></span><span id="secpkg_attr_authority"></span><dl> <dt>**SECPKG \_ \_Autorité attr**</dt> <dt>6</dt> </dl>                                                  | Le paramètre *pbuffer* contient un pointeur vers une structure d' [**\_ autorité SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_authoritya) .<br/> Interroge le nom de l’autorité d’authentification.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="SECPKG_ATTR_CLIENT_SPECIFIED_TARGET"></span><span id="secpkg_attr_client_specified_target"></span><dl> <dt>**SECPKG \_ \_ \_ \_ Cible spécifiée par le client attr**</dt> <dt>27</dt> </dl>     | Le paramètre *pbuffer* contient un pointeur vers une structure [**SecPkgContext \_ ClientSpecifiedTarget**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_clientspecifiedtarget) qui représente le nom de principal du service (SPN) de la cible initiale fournie par le client. <br/> Cette valeur est prise en charge uniquement lors de l’utilisation de liaisons de canal.<br/> **Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_CREDS_2"></span><span id="secpkg_attr_creds_2"></span><dl> <dt>**SECPKG \_ \_Références d’identification \_ 2**</dt> <dt>0x80000086</dt> </dl>                                              | Le paramètre *pbuffer* contient un pointeur vers une structure [**SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) qui spécifie les informations d’identification du client. <br/> Si les informations d’identification du client sont le nom d’utilisateur et le mot de passe, la mémoire tampon est une structure de [**\_ \_ connexion interactive KERB**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon) compressée.<br/> Si les informations d’identification du client sont le nom d’utilisateur et le code confidentiel de la carte à puce, la mémoire tampon est une structure de [**\_ \_ connexion de certificat KERB**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon) compressée.<br/> Si les informations d’identification du client sont des informations d’identification d’identité en ligne, la mémoire tampon est une structure EX2 de l' [**\_ \_ identité d’authentification \_ \_ winnt du sec**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) marshalée.<br/> Cet attribut est pris en charge uniquement sur le serveur CredSSP.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.<br/> |
| <span id="SECPKG_ATTR_DCE_INFO"></span><span id="secpkg_attr_dce_info"></span><dl> <dt>**SECPKG \_ \_ \_ Informations DCE d’attr**</dt> . <dt>3</dt> </dl>                                                    | Le paramètre *pbuffer* contient un pointeur vers une structure [**SecPkgContext \_ DceInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_dceinfo) .<br/> Requêtes pour les données d’autorisation utilisées par les services DCE.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_FLAGS"></span><span id="secpkg_attr_flags"></span><dl> <dt>**SECPKG \_ \_Indicateurs attr**</dt> <dt>14</dt> </dl>                                                             | Le paramètre *pbuffer* contient un pointeur vers une structure d' [**\_ indicateurs SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_flags) .<br/> Retourne des informations sur les indicateurs de contexte négociés.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="SECPKG_ATTR_KEY_INFO"></span><span id="secpkg_attr_key_info"></span><dl> <dt>**SECPKG \_ \_ \_ Informations sur la clé attr**</dt> <dt>5</dt> </dl>                                                    | Le paramètre *pbuffer* contient un pointeur vers une [**structure \_ KeyInfo SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_keyinfoa) .<br/> Interroge des informations sur les clés utilisées dans un [*contexte de sécurité*](../secgloss/s-gly.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SECPKG_ATTR_LAST_CLIENT_TOKEN_STATUS"></span><span id="secpkg_attr_last_client_token_status"></span><dl> <dt>**SECPKG \_ ATTR \_ dernier \_ \_ \_ État du jeton client**</dt> <dt>30</dt> </dl> | Le paramètre *pbuffer* contient un pointeur vers une structure [**SecPkgContext \_ LastClientTokenStatus**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lastclienttokenstatus) qui spécifie si le jeton de l’appel le plus récent à la fonction [**InitializeSecurityContext**](initializesecuritycontext--general.md) est le dernier jeton du client.<br/> **Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="SECPKG_ATTR_LIFESPAN"></span><span id="secpkg_attr_lifespan"></span><dl> <dt>**SECPKG \_ Durée de \_ vie**</dt> de l’attr <dt>2</dt> </dl>                                                     | Le paramètre *pbuffer* contient un pointeur vers une structure de durée de [**\_ vie SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lifespan) .<br/> Interroge l’étendue de la durée de vie du contexte.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="SECPKG_ATTR_LOCAL_CRED"></span><span id="secpkg_attr_local_cred"></span><dl> <dt>**SECPKG \_ attr \_ local \_ cred**</dt> </dl>                                                                                                     | Le paramètre *pbuffer* contient un pointeur vers une structure **SecPkgContext \_ LocalCredentialInfo** . (obsolète)<br/> Remplacé par SECPKG \_ attr \_ local \_ CERT \_ Context.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="SECPKG_ATTR_NAMES"></span><span id="secpkg_attr_names"></span><dl> <dt>**SECPKG \_ \_Noms attr**</dt> <dt>1</dt> </dl>                                                              | Le paramètre *pbuffer* contient un pointeur vers une structure de [**\_ noms SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_namesa) .<br/> Interroge le nom associé au contexte.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="SECPKG_ATTR_NATIVE_NAMES"></span><span id="secpkg_attr_native_names"></span><dl> <dt>**SECPKG \_ ATTR \_ , \_ noms natifs**</dt> <dt>13</dt> </dl>                                       | Le paramètre *pbuffer* contient un pointeur vers une structure [**SecPkgContext \_ NativeNames**](https://docs.microsoft.com/windows/win32/api/sspi/ns-sspi-_secpkgcontext_nativenamesa) .<br/> Retourne le nom de principal (CNAMe) du ticket sortant.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_NEGOTIATION_INFO"></span><span id="secpkg_attr_negotiation_info"></span><dl> <dt>**SECPKG \_ \_ \_ Informations de négociation d’attr**</dt> <dt>12</dt> </dl>                           | Le paramètre *pbuffer* contient un pointeur vers une structure [**SecPkgContext \_ NegotiationInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_negotiationinfoa) .<br/> Retourne des informations sur le [*package de sécurité*](../secgloss/s-gly.md) à utiliser avec le processus de négociation et l’état actuel de la négociation pour l’utilisation de ce package.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_ATTR_PACKAGE_INFO"></span><span id="secpkg_attr_package_info"></span><dl> <dt>**SECPKG \_ \_ \_ Informations sur le package attr**</dt> <dt>10</dt> </dl>                                       | Le paramètre *pbuffer* contient un pointeur vers une structure [**SecPkgContext \_ PackageInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .<br/> Retourne des informations sur le fournisseur de services partagés en cours d’utilisation.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_PASSWORD_EXPIRY"></span><span id="secpkg_attr_password_expiry"></span><dl> <dt>**SECPKG \_ \_ \_ Expiration du mot de passe attr**</dt> <dt>8</dt> </dl>                               | Le paramètre *pbuffer* contient un pointeur vers une structure [**SecPkgContext \_ PasswordExpiry**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_passwordexpiry) .<br/> Retourne les informations d’expiration du mot de passe.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_ROOT_STORE"></span><span id="secpkg_attr_root_store"></span><dl> <dt>**SECPKG \_ 0x55 \_ du \_ magasin racine attr**</dt> <dt></dt> </dl>                                           | Le paramètre *pbuffer* contient un pointeur vers **HCERTCONTEXT**. <br/> Recherche un contexte de certificat qui contient un certificat fourni par le magasin racine.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="SECPKG_ATTR_SESSION_KEY"></span><span id="secpkg_attr_session_key"></span><dl> <dt>**SECPKG \_ \_ \_ Clé de session d’attr**</dt> <dt>9</dt> </dl>                                           | Le paramètre *pbuffer* contient un pointeur vers une structure [**SecPkgContext \_ SessionKey**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sessionkey) .<br/> Retourne des informations sur la [*clé de session*](../secgloss/s-gly.md)s.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SECPKG_ATTR_SIZES"></span><span id="secpkg_attr_sizes"></span><dl> <dt>**SECPKG \_ \_Tailles d’attr**</dt> <dt>0</dt> </dl>                                                              | Le paramètre *pbuffer* contient un pointeur vers une structure de [**\_ tailles SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) .<br/> Interroge les tailles des structures utilisées dans les fonctions par message.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="SECPKG_ATTR_TARGET_INFORMATION"></span><span id="secpkg_attr_target_information"></span><dl> <dt>**SECPKG \_ \_ \_ Informations sur la cible d’attr**</dt> <dt>17</dt> </dl>                     | Le paramètre *pbuffer* contient un pointeur vers une structure [**SecPkgContext \_ TargetInformation**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_targetinformation) .<br/> Retourne des informations sur le nom du serveur distant.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*pbuffer* \[ à\]
</dt> <dd>

Pointeur vers une structure qui reçoit les attributs. Le type de structure pointé dépend de la valeur spécifiée dans le paramètre *ulAttribute* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction s’exécute correctement, la valeur de retour est s \_ E \_ OK.

Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro.

## <a name="remarks"></a>Remarques

La structure vers laquelle pointe le paramètre *pbuffer* varie en fonction de l’attribut interrogé. L’appelant doit allouer la structure *pbuffer* elle-même, mais le SSP alloue la mémoire nécessaire pour contenir les membres de taille variable de la structure *pbuffer* . La mémoire allouée par le fournisseur de services partagés peut être libérée en appelant la fonction [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .

Après la lecture du contexte de certificat \_ distant attr SECPKG ou de la \_ valeur de contexte de \_ \_ \_ certificat local SECPKG attr \_ \_ \_ , le membre **hCertStore** est défini sur un handle vers un magasin de certificats qui contient les certificats intermédiaires, le cas échéant. En outre, l’application est responsable de l’appel de [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) pour libérer la mémoire utilisée par le contexte de certificat.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>SSPI. h (include Security. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Noms Unicode et ANSI<br/>   | **QueryContextAttributesW** (Unicode) et **QueryContextAttributesA** (ANSI)<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**contexte du certificat \_**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[**\_Autorité SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_authoritya)
</dt> <dt>

[**SecPkgContext \_ ConnectionInfo**](/windows/win32/api/schannel/ns-schannel-secpkgcontext_connectioninfo)
</dt> <dt>

[**SecPkgContext \_ DceInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_dceinfo)
</dt> <dt>

[**SecPkgContext \_ IssuerListInfoEx**](/windows/win32/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex)
</dt> <dt>

[**SecPkgContext \_ KeyInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_keyinfoa)
</dt> <dt>

[**Durée de \_ vie SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lifespan)
</dt> <dt>

[**Noms de SecPkgContext \_**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_namesa)
</dt> <dt>

[**Tailles de SecPkgContext \_**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)
</dt> <dt>

[**SecPkgContext \_ StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes)
</dt> </dl>

 

 
