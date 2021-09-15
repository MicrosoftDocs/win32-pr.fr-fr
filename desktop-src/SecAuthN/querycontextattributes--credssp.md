---
description: Permet à une application de transport d’interroger le package de sécurité du fournisseur de support de sécurité des informations d’identification (CredSSP) pour certains attributs d’un contexte de sécurité.
ms.assetid: 4956c4ab-b71e-4960-b750-f3a79b87baac
title: QueryContextAttributes (CredSSP), fonction (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 191c3c8d3b2b5bd829aaf8eb45bacadbbd2bbade
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519080"
---
# <a name="querycontextattributes-credssp-function"></a>QueryContextAttributes (CredSSP) (fonction)

La fonction **QueryContextAttributes (CredSSP)** permet à une application de transport d’interroger le package de sécurité du fournisseur de support de sécurité des informations d’identification (CredSSP) pour certains [*attributs*](../secgloss/a-gly.md#_security_attribute_gly) d’un contexte de sécurité.

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

Handle vers le contexte de sécurité à interroger.

</dd> <dt>

*ulAttribute* \[ dans\]
</dt> <dd>

Attribut du contexte à retourner. Ce paramètre peut prendre les valeurs suivantes. Sauf spécification contraire, les attributs sont applicables à la fois au client et au serveur.



| Valeur                                                                                                                                                                                                                                                                                                   | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_ATTR_C_ACCESS_TOKEN"></span><span id="secpkg_attr_c_access_token"></span><dl> <dt>**SECPKG \_ 0x80000012 \_ \_ \_ jeton d’accès de l’attr C**</dt> <dt></dt> </dl>                                 | Le paramètre *pbuffer* contient un pointeur vers une structure [**SecPkgContext \_ AccessToken**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) qui spécifie le jeton d’accès pour le contexte de sécurité actuel.<br/> Cet attribut est pris en charge uniquement sur le serveur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_ATTR_C_FULL_ACCESS_TOKEN"></span><span id="secpkg_attr_c_full_access_token"></span><dl> <dt>**SECPKG \_ ATTR \_ C \_ \_ \_ jeton d’accès complet**</dt> <dt>0x80000082</dt> </dl>                 | Le paramètre *pbuffer* contient un pointeur vers une structure [**SecPkgContext \_ AccessToken**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) qui spécifie le jeton d’accès pour le contexte de sécurité actuel.<br/> Cet attribut est pris en charge uniquement sur le serveur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_ATTR_CERT_TRUST_STATUS"></span><span id="secpkg_attr_cert_trust_status"></span><dl> <dt>**SECPKG \_ ATTR \_ \_ \_ État**</dt> de l’approbation du certificat <dt>0x80000084</dt> </dl>                        | Le paramètre *pbuffer* contient un pointeur vers une structure d' [**\_ \_ État d’approbation de certificat**](/windows/win32/api/wincrypt/ns-wincrypt-cert_trust_status) qui spécifie des informations d’approbation sur le certificat.<br/> Cet attribut est pris en charge uniquement sur le client.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_CREDS"></span><span id="secpkg_attr_creds"></span><dl> <dt>**SECPKG \_ ATTR \_ CREDS**</dt> <dt>0x80000080</dt> </dl>                                                              | Le paramètre *pbuffer* contient un pointeur vers une structure [**SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) qui spécifie les informations d’identification du client.<br/> Les informations d’identification du client peuvent être un nom d’utilisateur et un mot de passe ou un nom d’utilisateur et un code confidentiel de carte à puce.<br/> Cet attribut est pris en charge uniquement sur le serveur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SECPKG_ATTR_CREDS_2"></span><span id="secpkg_attr_creds_2"></span><dl> <dt>**SECPKG \_ \_Références d’identification \_ 2**</dt> <dt>0x80000086</dt> </dl>                                                       | Le paramètre *pbuffer* contient un pointeur vers une structure [**SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) qui spécifie les informations d’identification du client. <br/> Si les informations d’identification du client sont le nom d’utilisateur et le mot de passe, la mémoire tampon est une structure de [**\_ \_ connexion interactive KERB**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon) compressée.<br/> Si les informations d’identification du client sont le nom d’utilisateur et le code confidentiel de la carte à puce, la mémoire tampon est une structure de [**\_ \_ connexion de certificat KERB**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon) compressée.<br/> Si les informations d’identification du client sont des informations d’identification d’identité en ligne, la mémoire tampon est une structure EX2 de l' [**\_ \_ identité d’authentification \_ \_ winnt du sec**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) marshalée.<br/> Cet attribut est pris en charge uniquement sur le serveur CredSSP.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.<br/> |
| <span id="SECPKG_ATTR_NEGOTIATION_PACKAGE"></span><span id="secpkg_attr_negotiation_package"></span><dl> <dt>**SECPKG \_ 0x80000081 \_ de \_ package de négociation attr**</dt> <dt></dt> </dl>                   | Le paramètre *pbuffer* contient un pointeur vers une structure [**SecPkgContext \_ PackageInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) qui spécifie le nom du package d’authentification négocié par le fournisseur [Microsoft Negotiate](microsoft-negotiate.md) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_ATTR_PACKAGE_INFO"></span><span id="secpkg_attr_package_info"></span><dl> <dt>**SECPKG \_ \_ \_ Informations sur le package attr**</dt> <dt>10</dt> </dl>                                                | Le paramètre *pbuffer* contient un pointeur vers une structure [**SecPkgContext \_ PackageInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa).<br/> Retourne des informations sur le fournisseur de services partagés en cours d’utilisation.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_SERVER_AUTH_FLAGS"></span><span id="secpkg_attr_server_auth_flags"></span><dl> <dt>**SECPKG \_ \_ \_ \_ Identificateurs d’authentification du serveur attr**</dt> <dt>0x80000083</dt> </dl>                        | Le paramètre *pbuffer* contient un pointeur vers une structure d' [**\_ indicateurs SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_flags) qui spécifie des informations sur les indicateurs dans le contexte de sécurité actuel.<br/> Cet attribut est pris en charge uniquement sur le client.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_SIZES"></span><span id="secpkg_attr_sizes"></span><dl> <dt>**SECPKG \_ \_Tailles d’attr**</dt> <dt>0x0</dt> </dl>                                                                     | Le paramètre *pbuffer* contient un pointeur vers une structure de [**\_ tailles SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) .<br/> Interroge les tailles des structures utilisées dans les fonctions par message et les échanges d’authentification.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="SECPKG_ATTR_SUBJECT_SECURITY_ATTRIBUTES"></span><span id="secpkg_attr_subject_security_attributes"></span><dl> <dt>**SECPKG \_ \_Attributs de \_ sécurité \_ de l’objet attr**</dt> <dt>124</dt> </dl> | Le paramètre *pbuffer* contient un pointeur vers une structure [**SecPkgContext \_ SubjectAttributes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_subjectattributes) .<br/> Cette valeur renvoie des informations sur les attributs de sécurité de la connexion.<br/> Cette valeur est prise en charge uniquement sur le serveur CredSSP.<br/> **Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pbuffer* \[ à\]
</dt> <dd>

Pointeur vers une structure qui reçoit les attributs. Le type de structure dépend de la valeur du paramètre *ulAttribute* .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, elle retourne SEC \_ E \_ OK.

Si la fonction échoue, elle peut retourner les codes d’erreur suivants.



| Code/valeur de retour                                                                                                                                                            | Description                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ E \_ \_ handle non valide**</dt> <dt>0x80100003</dt> </dl>       | Échec de la fonction. Le paramètre *phContext* spécifie un handle vers un contexte incomplet.<br/> |
| <dl> <dt>**S \_ E \_ 0x80090302 \_ fonction non prise en charge**</dt> <dt></dt> </dl> | Échec de la fonction. La valeur du paramètre *ulAttribute* n’est pas valide.<br/>                 |



 

## <a name="remarks"></a>Remarques

La structure vers laquelle pointe le paramètre *pbuffer* varie en fonction de l’attribut interrogé.

Alors que l’appelant doit allouer la structure *pbuffer* elle-même, le fournisseur de services partagés alloue la mémoire nécessaire pour contenir les membres de taille variable de la structure *pbuffer* . La mémoire allouée par le SSP doit être libérée par l’appel de la fonction [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                   |
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

[**SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds)
</dt> <dt>

[**Tailles de SecPkgContext \_**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)
</dt> </dl>

 

 
