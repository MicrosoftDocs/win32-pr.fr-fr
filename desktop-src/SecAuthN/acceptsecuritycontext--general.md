---
description: Active le composant serveur d’une application de transport pour établir un [*contexte de sécurité*](../secgloss/s-gly.md) entre le serveur et un client distant.
ms.assetid: eaa15fed-4438-4e43-9be3-aa100ca453c7
title: AcceptSecurityContext (général), fonction (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 41b3220e9304f63e1a6ac4f77b609e3cbbac8741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865733"
---
# <a name="acceptsecuritycontext-general-function"></a>AcceptSecurityContext (général) (fonction)

La fonction **AcceptSecurityContext (général)** permet au composant serveur d’une application de transport d’établir un [*contexte de sécurité*](../secgloss/s-gly.md) entre le serveur et un client distant. Le client distant utilise la fonction [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) pour démarrer le processus d’établissement d’un [*contexte de sécurité*](../secgloss/s-gly.md). Le serveur peut exiger un ou plusieurs jetons de réponse du client distant pour terminer l’établissement du [*contexte de sécurité*](../secgloss/s-gly.md).

Pour plus d’informations sur l’utilisation de cette fonction avec un fournisseur SSP ( [*Security Support Provider*](../secgloss/s-gly.md) ) spécifique, consultez les rubriques suivantes.



| Rubrique                                                                          | Description                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md)     | Autorise le composant serveur d’une application de transport à établir un [*contexte de sécurité*](../secgloss/s-gly.md) entre le serveur et un client distant à l’aide du protocole CredSSP (Credential Security Support Provider).<br/> |
| [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md)       | Active le composant serveur d’une application de transport pour établir un [*contexte de sécurité*](../secgloss/s-gly.md) entre le serveur et un client distant qui utilise le protocole Digest.<br/>                                                                                                                  |
| [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md)   | Active le composant serveur d’une application de transport pour établir un [*contexte de sécurité*](../secgloss/s-gly.md) entre le serveur et un client distant qui utilise Kerberos.<br/>                                                                                                                |
| [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) | Active le composant serveur d’une application de transport pour établir un [*contexte de sécurité*](../secgloss/s-gly.md) entre le serveur et un client distant qui utilise Negotiate.<br/>                                                                                                               |
| [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md)           | Active le composant serveur d’une application de transport pour établir un [*contexte de sécurité*](../secgloss/s-gly.md) entre le serveur et un client distant qui utilise NTLM.<br/>                                                                                                                    |
| [**AcceptSecurityContext (SChannel)**](acceptsecuritycontext--schannel.md)   | Active le composant serveur d’une application de transport pour établir un [*contexte de sécurité*](../secgloss/s-gly.md) entre le serveur et un client distant qui utilise Schannel.<br/>                                                                                                                |



 

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS SEC_Entry AcceptSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _Inout_opt_ PCtxtHandle    phContext,
  _In_opt_    PSecBufferDesc pInput,
  _In_        ULONG          fContextReq,
  _In_        ULONG          TargetDataRep,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Inout_opt_ PSecBufferDesc pOutput,
  _Out_       PULONG         pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*phCredential* \[ dans, facultatif\]
</dt> <dd>

Handle des informations d’identification du serveur. Le serveur appelle la fonction [**AcquireCredentialsHandle (général)**](acquirecredentialshandle--general.md) avec l’indicateur SECPKG \_ cred \_ entrant ou SECPKG \_ cred \_ défini pour récupérer ce handle.

</dd> <dt>

*phContext* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [CtxtHandle](sspi-handles.md) . Lors du premier appel à **AcceptSecurityContext (général)**, ce pointeur est **null**. Lors des appels suivants, *phContext* est le handle du contexte partiellement formé qui a été retourné dans le paramètre *phNewContext* par le premier appel.

</dd> <dt>

*pInput* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) générée par un appel client à [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) qui contient le descripteur de mémoire tampon d’entrée.

Lors de l’utilisation du SSP Schannel, le premier tampon doit être de type SECBUFFER \_ Token et contenir le jeton de sécurité reçu du client. La deuxième mémoire tampon doit être de type SECBUFFER \_ vide.

Lors de l’utilisation des SSP Negotiate, Kerberos ou NTLM, les informations de liaison de canal peuvent être spécifiées en passant une structure [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) de **\_ \_ liaisons de canaux** de type SecBuffer en plus des mémoires tampons générées par l’appel à la fonction [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) . Les informations de liaison de canal pour la mémoire tampon de liaison de canal peuvent être obtenues en appelant la fonction [**QueryContextAttributes (SChannel)**](querycontextattributes--schannel.md) sur le contexte Schannel utilisé par le client pour s’authentifier.

</dd> <dt>

*fContextReq* \[ dans\]
</dt> <dd>

Indicateurs de bits qui spécifient les attributs requis par le serveur pour établir le contexte. **Les indicateurs de bits** peuvent être combinés à l’aide d’opérations or au niveau du bit. Ce paramètre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                          | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_ALLOCATE_MEMORY"></span><span id="asc_req_allocate_memory"></span><dl> <dt>**\_demande ASC \_ allouer de la \_ mémoire**</dt> </dl>                                                  | Digest et Schannel allouent les tampons de sortie pour vous. Lorsque vous avez fini d’utiliser les tampons de sortie, libérez-les en appelant la fonction [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .<br/>                                                                                                                                                                                                                                                                                |
| <span id="ASC_REQ_ALLOW_MISSING_BINDINGS"></span><span id="asc_req_allow_missing_bindings"></span><dl> <dt>**la \_ demande ASC \_ autorise les \_ liaisons manquantes \_**</dt> </dl>                            | Indique que Digest ne requiert pas de liaisons de canal pour les canaux internes et externes. Cette valeur est utilisée pour la compatibilité descendante lorsque la prise en charge de la liaison de canal de point de terminaison n’est pas connue.<br/> Cette valeur s’exclut mutuellement avec les **\_ liaisons de \_ proxy \_ de demande ASC**.<br/> Cette valeur est prise en charge uniquement par le SSP Digest.<br/> **Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.<br/> <br/> |
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**\_confidentialité des demandes ASC \_**</dt> </dl>                                                   | Chiffrer et déchiffrer les messages. <br/> Le SSP Digest prend en charge cet indicateur pour SASL uniquement.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**connexion à la \_ demande ASC \_**</dt> </dl>                                                                  | Le [*contexte de sécurité*](../secgloss/s-gly.md) ne gère pas les messages de mise en forme.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ASC_REQ_DELEGATE"></span><span id="asc_req_delegate"></span><dl> <dt>**\_délégué req \_ ASC**</dt> </dl>                                                                        | Le serveur est autorisé à emprunter l’identité du client. Valide pour Kerberos. Ignorez cet indicateur pour la [*délégation avec restriction*](../secgloss/c-gly.md).<br/>                                                                                                                                                                                                                                                             |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**\_ \_ erreur étendue ASC \_ req**</dt> </dl>                                                     | Lorsque des erreurs se produisent, le tiers distant est averti.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ASC_REQ_HTTP__0x10000000_"></span><span id="asc_req_http__0x10000000_"></span><span id="ASC_REQ_HTTP__0X10000000_"></span><dl> <dt>**ASC \_ req \_ http (0x10000000)**</dt> </dl> | Utilisez Digest pour HTTP. Omettez cet indicateur pour utiliser Digest comme mécanisme SASL.<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="ASC_REQ_INTEGRITY"></span><span id="asc_req_integrity"></span><dl> <dt>**\_intégrité des demandes ASC \_**</dt> </dl>                                                                     | Signer des messages et vérifier les signatures.<br/> Schannel ne prend pas en charge cet indicateur.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="ASC_REQ_MUTUAL_AUTH"></span><span id="asc_req_mutual_auth"></span><dl> <dt>**\_ \_ authentification mutuelle des demandes ASC \_**</dt> </dl>                                                              | Le client doit fournir un certificat à utiliser pour l’authentification du client.<br/> Cet indicateur est pris en charge uniquement par Schannel.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="ASC_REQ_PROXY_BINDINGS"></span><span id="asc_req_proxy_bindings"></span><dl> <dt>**\_liaisons de \_ proxy de demande ASC \_**</dt> </dl>                                                     | Indique que le Digest requiert la liaison de canal.<br/> Cette valeur s’exclut mutuellement avec la **demande ASC qui \_ autorise les \_ \_ \_ liaisons manquantes**.<br/> Cette valeur est prise en charge uniquement par le SSP Digest.<br/> **Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.<br/> <br/>                                                                                                                                         |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**détection de la \_ RElecture de la demande ASC \_ \_**</dt> </dl>                                                        | Détecter les paquets relus.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**détection de la \_ séquence de demande ASC \_ \_**</dt> </dl>                                                  | Détecte les messages reçus en dehors de la séquence.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ASC_REQ_STREAM"></span><span id="asc_req_stream"></span><dl> <dt>**\_flux de demande ASC \_**</dt> </dl>                                                                              | Prend en charge une connexion orientée flux.<br/> Cet indicateur est pris en charge uniquement par Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |



 

Pour connaître les indicateurs d’attribut possibles et leurs significations, consultez [spécifications de contexte](context-requirements.md). Les indicateurs utilisés pour ce paramètre sont préfixés avec ASC \_ req, par exemple ASC \_ req \_ Delegate.

Les attributs demandés ne sont peut-être pas pris en charge par le client. Pour plus d’informations, consultez le paramètre *pfContextAttr* .

</dd> <dt>

*TargetDataRep* \[ dans\]
</dt> <dd>

Représentation des données, telle que l’ordonnancement des octets, sur la cible. Ce paramètre peut être SECURITY \_ native \_ DREP ou Security \_ Network \_ DREP.

Ce paramètre n’est pas utilisé avec les SSP Schannel ou Digest. Lorsque vous utilisez Schannel ou SSP Digest, spécifiez zéro pour ce paramètre.

</dd> <dt>

*phNewContext* \[ in, out, facultatif\]
</dt> <dd>

Pointeur vers une structure [CtxtHandle](sspi-handles.md) . Lors du premier appel à **AcceptSecurityContext (général)**, ce pointeur reçoit le nouveau handle de contexte. Lors des appels suivants, *phNewContext* peut être le même que le handle spécifié dans le paramètre *phContext* .

</dd> <dt>

*pOutput* \[ in, out, facultatif\]
</dt> <dd>

Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) qui contient le descripteur de mémoire tampon de sortie. Cette mémoire tampon est envoyée au client pour l’entrée dans des appels supplémentaires à [**InitializeSecurityContext (général)**](initializesecuritycontext--general.md). Une mémoire tampon de sortie peut être générée même si la fonction retourne SEC \_ E \_ OK. Toute mémoire tampon générée doit être renvoyée à l’application cliente.

Lors de l’utilisation de Schannel, en sortie, cette mémoire tampon reçoit un jeton pour le [*contexte de sécurité*](../secgloss/s-gly.md). Le jeton doit être envoyé au client. La fonction peut également retourner une mémoire tampon de type SECBUFFER \_ extra. En outre, l’appelant doit passer une mémoire tampon de type **\_ alerte SECBUFFER**. Lors de la sortie, si une alerte est générée, cette mémoire tampon contient des informations sur cette alerte et la fonction échoue.

</dd> <dt>

*pfContextAttr* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit un jeu d’indicateurs binaires qui indiquent les attributs du contexte établi. Pour obtenir une description des différents attributs, consultez [spécifications de contexte](context-requirements.md). Les indicateurs utilisés pour ce paramètre sont préfixés par ASC \_ RET, par exemple ASC \_ RET \_ Delegate.

Ne vérifiez pas les attributs liés à la sécurité jusqu’à ce que l’appel de fonction final soit retourné avec succès. Les indicateurs d’attribut non liés à la sécurité, tels que l' \_ indicateur ASC RET \_ allouée la \_ mémoire, peuvent être vérifiés avant le retour final.

</dd> <dt>

*ptsTimeStamp* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une structure d' [**horodatage**](timestamp.md) qui reçoit l’heure d’expiration du contexte. Nous recommandons que le [*package de sécurité*](../secgloss/s-gly.md) retourne toujours cette valeur en heure locale.

Ce paramètre est défini sur une durée maximale constante. Il n’y a pas de délai d’expiration pour les informations d’identification ou les informations d’identification du [*contexte de sécurité*](../secgloss/s-gly.md)Digest ou lors de l’utilisation du SSP Digest.

Cette option est facultative lors de l’utilisation du SSP Schannel. Lorsque le tiers distant a fourni un certificat à utiliser pour l’authentification, ce paramètre reçoit l’heure d’expiration de ce certificat. Si aucun certificat n’a été fourni, une valeur de temps maximale est retournée.

> [!Note]  
> Jusqu’au dernier appel du processus d’authentification, l’heure d’expiration du contexte peut être incorrecte, car des informations supplémentaires seront fournies lors des étapes ultérieures de la négociation. Par conséquent, *ptsTimeStamp* doit avoir la **valeur null** jusqu’au dernier appel à la fonction.

 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne l’une des valeurs suivantes.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Code/valeur de retour</th><th>Description</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_BAD_BINDINGS</strong></dt> <dt>0x80090346L</dt> </dl></td><td>Échec de la fonction. La stratégie de liaison de canal n’a pas été satisfaite.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INCOMPLETE_MESSAGE</strong></dt> <dt>0x80090318L</dt> </dl></td><td>La fonction a réussi. Les données de la mémoire tampon d’entrée sont incomplètes. L’application doit lire les données supplémentaires à partir du client et appeler à nouveau [<strong>AcceptSecurityContext (General)</strong>] (AcceptSecurityContext--General.MD).<br/> Cette valeur peut être retournée lors de l’utilisation du SSP Schannel. Pour plus d’informations sur cette valeur de retour, consultez [<strong>AcceptSecurityContext (SChannel)</strong>] (AcceptSecurityContext--Schannel.MD).<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300L</dt> </dl></td><td>Échec de la fonction. La mémoire disponible est insuffisante pour terminer l’action demandée.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304L</dt> </dl></td><td>Échec de la fonction. Une erreur qui n’a pas été mappée à un code d’erreur SSPI s’est produite.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003L</dt> </dl></td><td>Échec de la fonction. Le handle passé à la fonction n’est pas valide.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308L</dt> </dl></td><td>Échec de la fonction. Le jeton passé à la fonction n’est pas valide.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030CL</dt> </dl></td><td>L’ouverture de session a échoué.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311L</dt> </dl></td><td>Échec de la fonction. Aucune autorité n’a pu être contactée pour l’authentification. Cela peut être dû aux conditions suivantes :<br/><ul><li>Le nom de domaine du tiers d’authentification est incorrect.</li><li>Le domaine n’est pas disponible.</li><li>La relation d’approbation a échoué.</li></ul></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_NO_CREDENTIALS</strong></dt> <dt>0x8009030EL</dt> </dl></td><td>Échec de la fonction. Le descripteur des informations d’identification spécifié dans le paramètre <em>phCredential</em> n’est pas valide. Cette valeur peut être retournée lors de l’utilisation du SSP condensé ou Schannel.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000L</dt> </dl></td><td>La fonction a réussi. Le [*contexte de sécurité*](../secgloss/s-gly.md) reçu du client a été accepté. Si un jeton de sortie a été généré par la fonction, il doit être envoyé au processus client.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_SECURITY_QOS_FAILED</strong></dt> <dt>0x80090332L</dt> </dl></td><td>Échec de la fonction. Un indicateur d’attribut de contexte non valide a été spécifié dans le paramètre <em>fContextReq</em> . Cette valeur peut être retournée lors de l’utilisation du SSP Digest.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_UNSUPPORTED_FUNCTION</strong></dt> <dt>0x80090302L</dt> </dl></td><td>Échec de la fonction. Un indicateur d’attribut de contexte qui n’est pas valide (ASC_REQ_DELEGATE ou ASC_REQ_PROMPT_FOR_CREDS) a été spécifié dans le paramètre <em>fContextReq</em> . Cette valeur peut être retournée lors de l’utilisation du SSP Schannel.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314L</dt> </dl></td><td>La fonction a réussi. Le serveur doit appeler [<strong>CompleteAuthToken</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-CompleteAuthToken) et transmettre le jeton de sortie au client. Le serveur attend ensuite un jeton de retour du client et effectue ensuite un autre appel à [<strong>AcceptSecurityContext (General)</strong>] (AcceptSecurityContext--General.MD). <br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313L</dt> </dl></td><td>La fonction a réussi. Le serveur doit terminer la génération du message à partir du client, puis appeler la fonction [<strong>CompleteAuthToken</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-CompleteAuthToken).<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312L</dt> </dl></td><td>La fonction a réussi. Le serveur doit envoyer le jeton de sortie au client et attendre un jeton retourné. Le jeton retourné doit être passé dans <em>pInput</em> pour un autre appel à [<strong>AcceptSecurityContext (General)</strong>] (AcceptSecurityContext--General.MD).<br/></td></tr><tr class="even"><td><dl> <dt><strong>STATUS_LOGON_FAILURE</strong></dt> <dt>0xC000006DL</dt> </dl></td><td>Échec de la fonction. La fonction [<strong>AcceptSecurityContext (General)</strong>] (AcceptSecurityContext--General.MD) a été appelée après l’établissement du contexte spécifié. Cette valeur peut être retournée lors de l’utilisation du SSP Digest.<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>Notes

La fonction **AcceptSecurityContext (General)** est l’équivalent serveur de la fonction [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) .

Lorsque le serveur reçoit une demande d’un client, le serveur utilise le paramètre *fContextReq* pour spécifier ce qu’il requiert de la session. De cette manière, un serveur peut spécifier que les clients doivent être en mesure d’utiliser une session confidentielle ou contrôlée par [*l’intégrité*](../secgloss/i-gly.md), et il peut rejeter des clients qui ne répondent pas à cette demande. En guise d’alternative, un serveur ne peut nécessiter rien, et tout ce que le client peut fournir ou nécessite est retourné dans le paramètre *pfContextAttr* .

Pour un package qui prend en charge l’authentification à plusieurs jambes, telle que l’authentification mutuelle, la séquence d’appel est la suivante :

1.  Le client transmet un jeton au serveur.
2.  Le serveur appelle **AcceptSecurityContext (général)** la première fois, qui génère un jeton de réponse qui est ensuite envoyé au client.
3.  Le client reçoit le jeton et le passe à [**InitializeSecurityContext (général)**](initializesecuritycontext--general.md). Si **InitializeSecurityContext (General)** retourne sec \_ E \_ OK, l’authentification mutuelle est terminée et une session sécurisée peut commencer. Si **InitializeSecurityContext (General)** retourne un code d’erreur, la négociation de l’authentification mutuelle se termine. Dans le cas contraire, le jeton de sécurité retourné par **InitializeSecurityContext (General)** est envoyé au client et les étapes 2 et 3 sont répétées.

Les paramètres *fContextReq* et *pfContextAttr* sont des masques de masques qui représentent différents attributs de contexte. Pour obtenir une description des différents attributs, consultez [spécifications de contexte](context-requirements.md).

> [!Note]  
> Le paramètre *pfContextAttr* est valide en cas de retour réussi, mais uniquement lors du retour final réussi, vous devez examiner les indicateurs relatifs aux aspects de sécurité du contexte. Les retours intermédiaires peuvent définir, par exemple, \_ l' \_ indicateur ISC RET allouée \_ Memory.

 

L’appelant est chargé de déterminer si les attributs de contexte finaux sont suffisants. Si, par exemple, la confidentialité (chiffrement) a été demandée mais n’a pas pu être établie, certaines applications peuvent choisir d’arrêter immédiatement la connexion. Si le [*contexte de sécurité*](../secgloss/s-gly.md) ne peut pas être établi, le serveur doit libérer le contexte partiellement créé en appelant la fonction [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) . Pour plus d’informations sur l’appel de la fonction **DeleteSecurityContext** , consultez **DeleteSecurityContext**.

Une fois le [*contexte de sécurité*](../secgloss/s-gly.md) établi, l’application serveur peut utiliser la fonction [**QuerySecurityContextToken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) pour récupérer un handle vers le compte d’utilisateur auquel le certificat client a été mappé. En outre, le serveur peut utiliser la fonction [**ImpersonateSecurityContext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) pour emprunter l’identité de l’utilisateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>SSPI. h (include Security. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**InitializeSecurityContext (général)**](initializesecuritycontext--general.md)
</dt> </dl>

 

 
