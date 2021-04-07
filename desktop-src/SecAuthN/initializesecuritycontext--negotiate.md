---
description: Initie le [*contexte de sécurité*](../secgloss/s-gly.md) côté client et sortant à partir d’un handle d’informations d’identification à l’aide de la [*délégation conpressionnelle*](../secgloss/s-gly.md)Negotiate.
ms.assetid: 031b0e82-f246-4291-aed3-f443ab152e00
title: Fonction InitializeSecurityContext (Negotiate) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: f4fd8c68896f10627ff1d66c3f576ca06d67e029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864050"
---
# <a name="initializesecuritycontext-negotiate-function"></a>Fonction InitializeSecurityContext (Negotiate)

La fonction **InitializeSecurityContext (Negotiate)** initie le côté client et le [*contexte de sécurité*](../secgloss/s-gly.md) sortant à partir d’un handle d’informations d’identification. La fonction est utilisée pour créer un [*contexte de sécurité*](../secgloss/s-gly.md) entre l’application cliente et un homologue distant. **InitializeSecurityContext (Negotiate)** retourne un jeton que le client doit passer à l’homologue distant, que l’homologue à son tour soumet à l’implémentation de sécurité locale par le biais de l’appel de [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) . Le jeton généré doit être considéré comme opaque par tous les appelants.

En règle générale, la fonction **InitializeSecurityContext (Negotiate)** est appelée dans une boucle jusqu’à ce qu’un [*contexte de sécurité*](../secgloss/s-gly.md) suffisant soit établi.

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS SEC_Entry InitializeSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    SEC_CHAR       *pszTargetName,
  _In_        ULONG          fContextReq,
  _In_        ULONG          Reserved1,
  _In_        ULONG          TargetDataRep,
  _In_opt_    PSecBufferDesc pInput,
  _In_        ULONG          Reserved2,
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

Handle des informations d’identification retournées par [**AcquireCredentialsHandle (Negotiate)**](acquirecredentialshandle--negotiate.md). Ce descripteur est utilisé pour générer le [*contexte de sécurité*](../secgloss/s-gly.md). La fonction **InitializeSecurityContext (Negotiate)** requiert au moins des informations d’identification sortantes.

</dd> <dt>

*phContext* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une structure [CtxtHandle](sspi-handles.md) . Lors du premier appel à **InitializeSecurityContext (Negotiate)**, ce pointeur est **null**. Lors du deuxième appel, ce paramètre est un pointeur vers le handle vers le contexte partiellement formé retourné dans le paramètre *phNewContext* par le premier appel.

</dd> <dt>

*pszTargetName* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui indique le nom de principal du service (SPN) ou le [*contexte de sécurité*](../secgloss/s-gly.md) du serveur de destination.

Les applications doivent fournir un SPN valide pour aider à atténuer les attaques par relecture.

</dd> <dt>

*fContextReq* \[ dans\]
</dt> <dd>

Indicateurs de bits qui indiquent les demandes pour le contexte. Tous les packages ne peuvent pas prendre en charge toutes les exigences. Les indicateurs utilisés pour ce paramètre sont précédés de la \_ demande ISC \_ , par exemple, ISC \_ req \_ Delegate. Ce paramètre peut être un ou plusieurs des indicateurs d’attributs suivants.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valeur</th><th>Signification</th></tr></thead><tbody><tr class="odd"><td><span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt> </dl></td><td>Le [*package de sécurité*](../secgloss/s-gly.md) alloue des tampons de sortie pour vous. Lorsque vous avez fini d’utiliser les tampons de sortie, libérez-les en appelant la fonction [<strong>FreeContextBuffer</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-freecontextbuffer).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl> <dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt> </dl></td><td>Chiffrez les messages à l’aide de la fonction [<strong>EncryptMessage</strong>] (EncryptMessage--General.MD).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt><strong>ISC_REQ_CONNECTION</strong></dt> </dl></td><td>Le [*contexte de sécurité*](../secgloss/s-gly.md) ne gère pas les messages de mise en forme. Il s’agit de la valeur par défaut.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt><strong>ISC_REQ_DELEGATE</strong></dt> </dl></td><td>Le serveur peut utiliser le contexte pour s’authentifier auprès d’autres serveurs en tant que client. L’indicateur de ISC_REQ_MUTUAL_AUTH doit être défini pour que cet indicateur fonctionne. Valide pour Kerberos. Ignorez cet indicateur pour la [*délégation avec restriction*](../secgloss/c-gly.md).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt> </dl></td><td>Lorsque des erreurs se produisent, le tiers distant est averti.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl> <dt><strong>ISC_REQ_INTEGRITY</strong></dt> </dl></td><td>Signer des messages et vérifier des signatures à l’aide des fonctions [<strong>EncryptMessage</strong>] (EncryptMessage--General.MD) et [<strong>MakeSignature</strong>] (makesignature.MD).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt> </dl></td><td>La stratégie d’authentification mutuelle du service sera satisfaite.<br/><blockquote>[!Caution]<br />
Cela ne signifie pas nécessairement que l’authentification mutuelle est effectuée, mais uniquement que la stratégie d’authentification du service est satisfaite. Pour vous assurer que l’authentification mutuelle est effectuée, appelez la fonction [<strong>QueryContextAttributes (Negotiate)</strong>] (QueryContextAttributes--Negotiate.MD).</blockquote><br/></td></tr><tr class="even"><td><span id="ISC_REQ_NO_INTEGRITY"></span><span id="isc_req_no_integrity"></span><dl> <dt><strong>ISC_REQ_NO_INTEGRITY</strong></dt> </dl></td><td>Si cet indicateur est défini, l’indicateur d' <strong>ISC_REQ_INTEGRITY</strong> est ignoré.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl> <dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt> </dl></td><td>Détectez les messages relus qui ont été encodés à l’aide des fonctions [<strong>EncryptMessage</strong>] (EncryptMessage--General.MD) ou [<strong>MakeSignature</strong>] (makesignature.MD).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt> </dl></td><td>Détecte les messages reçus en dehors de la séquence.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt><strong>ISC_REQ_STREAM</strong></dt> </dl></td><td>Prend en charge une connexion orientée flux.<br/></td></tr></tbody></table>



 

Les attributs demandés ne sont peut-être pas pris en charge par le client. Pour plus d’informations, consultez le paramètre *pfContextAttr* .

Pour plus d’informations sur les différents attributs, consultez [spécifications de contexte](context-requirements.md).

</dd> <dt>

*Reserved1* \[ dans\]
</dt> <dd>

Ce paramètre est réservé et doit avoir la valeur zéro.

</dd> <dt>

*TargetDataRep* \[ dans\]
</dt> <dd>

Représentation des données, telle que l’ordonnancement des octets, sur la cible. Ce paramètre peut être SECURITY \_ native \_ DREP ou Security \_ Network \_ DREP.

</dd> <dt>

*pInput* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) qui contient des pointeurs vers les mémoires tampons fournies comme entrée au package. À moins que le contexte client n’ait été initié par le serveur, la valeur de ce paramètre doit être **null** lors du premier appel à la fonction. Lors des appels suivants à la fonction ou lorsque le contexte client a été initié par le serveur, la valeur de ce paramètre est un pointeur vers une mémoire tampon allouée avec suffisamment de mémoire pour contenir le jeton retourné par l’ordinateur distant.

</dd> <dt>

*Reserved2* \[ dans\]
</dt> <dd>

Ce paramètre est réservé et doit avoir la valeur zéro.

</dd> <dt>

*phNewContext* \[ in, out, facultatif\]
</dt> <dd>

Pointeur vers une structure [CtxtHandle](sspi-handles.md) . Lors du premier appel à **InitializeSecurityContext (Negotiate)**, ce pointeur reçoit le nouveau handle de contexte. Lors du deuxième appel, *phNewContext* peut être le même que le handle spécifié dans le paramètre *phContext* .

</dd> <dt>

*pOutput* \[ in, out, facultatif\]
</dt> <dd>

Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) qui contient des pointeurs vers la structure [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) qui reçoit les données de sortie. Si une mémoire tampon a été tapée comme s \_ ReadWrite dans l’entrée, elle y figurera à la sortie. Le système alloue une mémoire tampon pour le jeton de sécurité si elle est demandée (par le biais de la \_ demande ISC \_ allocate \_ Memory) et remplit l’adresse dans le descripteur de mémoire tampon du jeton de sécurité.

</dd> <dt>

*pfContextAttr* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit un jeu d’indicateurs binaires qui indiquent les [*attributs*](../secgloss/a-gly.md#_security_attribute_gly) du contexte établi. Pour obtenir une description des différents attributs, consultez [spécifications de contexte](context-requirements.md).

Les indicateurs utilisés pour ce paramètre sont préfixés par ISC \_ RET, par exemple ISC \_ RET \_ Delegate. Pour obtenir la liste des valeurs valides, consultez le paramètre *fContextReq* .

Ne vérifiez pas les attributs liés à la sécurité jusqu’à ce que l’appel de fonction final soit retourné avec succès. Les indicateurs d’attribut qui ne sont pas liés à la sécurité, tels que l' \_ indicateur ASC RET \_ allouée la \_ mémoire, peuvent être vérifiés avant le retour final.

> [!Note]  
> Des attributs de contexte particuliers peuvent changer pendant la négociation avec un homologue distant.

 

</dd> <dt>

*ptsExpiry* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une structure d' [**horodatage**](timestamp.md) qui reçoit l’heure d’expiration du contexte. Il est recommandé que le [*package de sécurité*](../secgloss/s-gly.md) retourne toujours cette valeur en heure locale. Ce paramètre est facultatif et la **valeur null** doit être transmise pour les clients à courte durée de vie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la fonction retourne l’un des codes de réussite suivants.



| Code de retour                                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ OK**</dt> </dl>                      | Le [*contexte de sécurité*](../secgloss/s-gly.md) a été initialisé avec succès. Il n’est pas nécessaire d’avoir un autre appel [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) . Si la fonction retourne un jeton de sortie, autrement dit, si le \_ jeton SECBUFFER dans *pOutput* a une longueur différente de zéro, ce jeton doit être envoyé au serveur.<br/> |
| <dl> <dt>**s \_ j’ai \_ terminé \_ et je \_ continue**</dt> </dl> | Le client doit appeler [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) , puis transmettre la sortie au serveur. Le client attend ensuite un jeton retourné et le passe, dans un autre appel, à [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md).<br/>                                                                                                                                  |
| <dl> <dt>**s \_ \_ terminées \_**</dt> </dl>        | Le client doit terminer la génération du message, puis appeler la fonction [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) .<br/>                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**SEC \_ je \_ continue à avoir \_ besoin**</dt> </dl>        | Le client doit envoyer le jeton de sortie au serveur et attendre un jeton de retour. Le jeton retourné est ensuite passé dans un autre appel à [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md). Le jeton de sortie peut être vide.<br/>                                                                                                                                                       |



 

Si la fonction échoue, la fonction retourne l’un des codes d’erreur suivants.



| Code de retour                                                                                                          | Description                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**s \_ E \_ mémoire insuffisante \_**</dt> </dl>          | La mémoire disponible est insuffisante pour terminer l’action demandée.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**SEC \_ E \_ \_ erreur interne**</dt> </dl>               | Une erreur qui n’a pas été mappée à un code d’erreur SSPI s’est produite.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>**SEC \_ E \_ handle non valide \_**</dt> </dl>               | Le handle passé à la fonction n’est pas valide.<br/>                                                                                                                                                                                                                                          |
| <dl> <dt>**s \_ E \_ jeton non valide \_**</dt> </dl>                | L’erreur est due à un jeton d’entrée incorrect, tel qu’un jeton endommagé en transit, un jeton de taille incorrecte ou un jeton passé dans la [*délégation*](../secgloss/s-gly.md)conformée incorrecte. Le passage d’un jeton au mauvais package peut se produire si le client et le serveur n’ont pas négocié la [*délégation*](../secgloss/s-gly.md)appropriée.<br/> |
| <dl> <dt>**s \_ \_ ouverture de session \_ refusée**</dt> </dl>                 | L’ouverture de session a échoué.<br/>                                                                                                                                                                                                                                                                        |
| <dl> <dt>**s \_ E \_ aucune \_ autorité d’authentification \_**</dt> </dl> | Aucune autorité n’a pu être contactée pour l’authentification. Le nom de domaine du tiers d’authentification peut être incorrect, le domaine peut être inaccessible ou une relation d’approbation a peut-être échoué.<br/>                                                                                  |
| <dl> <dt>**s \_ E \_ aucune \_ information d’identification**</dt> </dl>               | Aucune information d’identification n’est disponible dans la [*délégation conpressionnelle*](../secgloss/s-gly.md).<br/>                                                                                                                                                  |
| <dl> <dt>**\_cible s \_ E \_ inconnu**</dt> </dl>               | La cible n’a pas été reconnue.<br/>                                                                                                                                                                                                                                                           |
| <dl> <dt>**SEC \_ E \_ fonction non prise en charge \_**</dt> </dl>         | Un indicateur d’attribut de contexte non valide (ISC \_ req \_ Delegate ou ISC \_ req \_ prompt \_ pour \_ CREDS) a été spécifié dans le paramètre *fContextReq* .<br/>                                                                                                                                            |
| <dl> <dt>**SEC \_ E \_ \_ principal erroné**</dt> </dl>              | Le principal qui a reçu la demande d’authentification n’est pas le même que celui passé dans le paramètre *pszTargetName* . Cela indique un échec de l’authentification mutuelle.<br/>                                                                                                          |



 

## <a name="remarks"></a>Notes

L’appelant est chargé de déterminer si les attributs de contexte finaux sont suffisants. Si, par exemple, la confidentialité a été demandée mais n’a pas pu être établie, certaines applications peuvent choisir d’arrêter immédiatement la connexion.

Si les attributs du [*contexte de sécurité*](../secgloss/s-gly.md) ne sont pas suffisants, le client doit libérer le contexte partiellement créé en appelant la fonction [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) .

La fonction **InitializeSecurityContext (Negotiate)** est utilisée par un client pour initialiser un contexte sortant.

Pour un [*contexte de sécurité*](../secgloss/s-gly.md)à deux jambes, la séquence appelante est la suivante :

1.  Le client appelle la fonction avec *phContext* défini sur **null** et remplit le descripteur de mémoire tampon avec le message d’entrée.
2.  Le [*package de sécurité*](../secgloss/s-gly.md) examine les paramètres et construit un jeton opaque, en le plaçant dans l’élément de jeton dans le tableau de mémoires tampons. Si le paramètre *fContextReq* comprend l' \_ indicateur ISC req \_ allocate \_ Memory, le [*package de sécurité*](../secgloss/s-gly.md) alloue la mémoire et retourne le pointeur dans l’élément de jeton.
3.  Le client envoie le jeton retourné dans la mémoire tampon *pOutput* au serveur cible. Le serveur transmet ensuite le jeton en tant qu’argument d’entrée dans un appel à la fonction [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) .
4.  [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) peut retourner un jeton, que le serveur envoie au client pour un deuxième appel à **InitializeSecurityContext (Negotiate)** si le premier appel a retourné sec \_ \_ \_ .

Pour un contexte de [*sécurité*](../secgloss/s-gly.md)à plusieurs jambes, tel que l’authentification mutuelle, la séquence d’appel est la suivante :

1.  Le client appelle la fonction comme décrit précédemment, mais le package renvoie le code de réussite de la procédure de reprise de la SEC \_ \_ \_ .
2.  Le client envoie le jeton de sortie au serveur et attend la réponse du serveur.
3.  Lors de la réception de la réponse du serveur, le client appelle à nouveau **InitializeSecurityContext (Negotiate)** , avec *phContext* défini sur le descripteur retourné à partir du dernier appel. Le jeton reçu du serveur est fourni dans le paramètre *pInput* .

Si le serveur a répondu, le package de [*sécurité*](../secgloss/s-gly.md) retourne sec \_ E \_ OK et une session sécurisée est établie.

Si la fonction retourne l’une des réponses d’erreur, la réponse du serveur n’est pas acceptée et la session n’est pas établie.

Si la fonction retourne SEC \_ i \_ continue \_ needed, sec \_ i \_ Completed \_ , ou sec \_ i \_ Completed \_ et \_ continue, les étapes 2 et 3 sont répétées.

Pour initialiser un [*contexte de sécurité*](../secgloss/s-gly.md), plusieurs appels à cette fonction peuvent être requis, en fonction du mécanisme d’authentification sous-jacent, ainsi que des choix spécifiés dans le paramètre *fContextReq* .

Les paramètres *fContextReq* et *pfContextAttributes* sont des masques de masques qui représentent différents attributs de contexte. Pour obtenir une description des différents attributs, consultez [spécifications de contexte](context-requirements.md). Le paramètre *pfContextAttributes* est valide en cas de retour réussi, mais uniquement lors du retour final réussi, vous devez examiner les indicateurs qui se rapportent aux aspects de sécurité du contexte. Les retours intermédiaires peuvent définir, par exemple, \_ l' \_ indicateur ISC RET allouée \_ Memory.

Si l’indicateur d’identification des informations d’identification \_ \_ fournies par l’ISC \_ \_ est défini, le [*package de sécurité*](../secgloss/s-gly.md) doit rechercher un type de \_ tampon SECBUFFER pkg \_ params dans la mémoire tampon d’entrée *pInput* . Il ne s’agit pas d’une solution générique, mais elle permet un appariement renforcé du [*package de sécurité*](../secgloss/s-gly.md) et de l’application, le cas échéant.

Si la \_ demande ISC \_ allocate \_ Memory a été spécifiée, l’appelant doit libérer la mémoire en appelant la fonction [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .

Par exemple, le jeton d’entrée peut être le défi d’un gestionnaire de réseau local. Dans ce cas, le jeton de sortie est la réponse chiffrée NTLM à la stimulation.

L’action effectuée par le client dépend du code de retour de cette fonction. Si le code de retour est SEC \_ E \_ OK, il n’y aura aucun deuxième appel **InitializeSecurityContext (Negotiate)** et aucune réponse du serveur ne sera attendue. Si le code de retour est \_ sec \_ , je continue \_ nécessaire, le client attend un jeton en réponse du serveur et le transmet dans un deuxième appel à **InitializeSecurityContext (Negotiate)**. Le code de retour de SEC \_ I \_ \_ requis indique que le client doit terminer la génération du message et appeler la fonction [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) . Les secondes \_ que j’ai \_ effectuées \_ et qui \_ poursuivent le code incorporent ces deux actions.

Si **InitializeSecurityContext (Negotiate)** renvoie une réussite sur le premier appel (ou uniquement), l’appelant doit finalement appeler la fonction [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) sur le handle retourné, même si l’appel échoue sur un tronçon ultérieur de l’échange d’authentification.

Le client peut appeler **InitializeSecurityContext (Negotiate)** une fois qu’il s’est terminé avec succès. Cela indique au [*package de sécurité*](../secgloss/s-gly.md) qu’une réauthentification est souhaitée.

Les appelants en mode noyau présentent les différences suivantes : le nom cible est une chaîne [*Unicode*](../secgloss/u-gly.md) qui doit être allouée dans la mémoire virtuelle à l’aide de [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc); elle ne doit pas être allouée à partir du pool. Les mémoires tampons transmises et fournies dans *pInput* et *pOutput* doivent être dans la mémoire virtuelle, et non dans le pool.

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

[**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md)
</dt> <dt>

[**AcquireCredentialsHandle (Negotiate)**](acquirecredentialshandle--negotiate.md)
</dt> <dt>

[**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)
</dt> <dt>

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
