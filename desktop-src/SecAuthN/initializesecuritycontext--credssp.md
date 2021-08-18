---
description: Initie le contexte de sécurité côté client et sortant à partir d’un handle d’informations d’identification.
ms.assetid: f3d8c07b-db28-4f26-ba29-8733fc95bdb5
title: InitializeSecurityContext (CredSSP), fonction (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 5ba38dd10552f90ecfcc5045b96edc5e62aff1f8a2beec0f2a728fc1f0be8c52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015989"
---
# <a name="initializesecuritycontext-credssp-function"></a>Fonction InitializeSecurityContext (CredSSP)

La fonction **InitializeSecurityContext (CredSSP)** initie le contexte de sécurité côté client et sortant à partir d’un handle d’informations d’identification. La fonction génère un contexte de sécurité entre l’application cliente et un homologue distant. **InitializeSecurityContext (CredSSP)** retourne un jeton que le client doit passer à l’homologue distant. l’homologue à son tour soumet ce jeton à l’implémentation de sécurité locale par le biais de l’appel [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) . Le jeton généré doit être considéré comme opaque par tous les appelants.

En règle générale, la fonction **InitializeSecurityContext (CredSSP)** est appelée dans une boucle jusqu’à ce qu’un contexte de sécurité suffisant soit établi.

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS SEC_ENTRY InitializeSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    SEC_CHAR       *pszTargetName,
  _In_        unsigned long  fContextReq,
  _Reserved_  unsigned long  Reserved1,
  _In_        unsigned long  TargetDataRep,
  _Inout_opt_ PSecBufferDesc pInput,
  _In_        unsigned long  Reserved2,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Out_opt_   PSecBufferDesc pOutput,
  _Out_       unsigned long  *pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*phCredential* \[ dans, facultatif\]
</dt> <dd>

Handle des informations d’identification retournées par [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md). Ce descripteur est utilisé pour générer le contexte de sécurité. La fonction **InitializeSecurityContext (CredSSP)** requiert au moins des informations d’identification sortantes.

</dd> <dt>

*phContext* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une structure [CtxtHandle](sspi-handles.md) . Lors du premier appel à **InitializeSecurityContext (CredSSP)**, ce pointeur est **null**. Lors du deuxième appel, ce paramètre est un pointeur vers le handle vers le contexte partiellement formé retourné dans le paramètre *phNewContext* par le premier appel.

Lors du premier appel à **InitializeSecurityContext (CredSSP)**, spécifiez **null**. Lors des appels ultérieurs, spécifiez le jeton reçu dans le paramètre *phNewContext* après le premier appel à cette fonction.

</dd> <dt>

*pTargetName* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui identifie de façon unique le serveur cible. Schannel utilise cette valeur pour vérifier le certificat du serveur. Schannel utilise également cette valeur pour localiser la session dans le cache de session lors de la réétablissement d’une connexion. La session mise en cache est utilisée uniquement si toutes les conditions suivantes sont remplies :

-   Le nom de la cible est le même.
-   L’entrée du cache n’a pas expiré.
-   Le processus d’application qui appelle la fonction est le même.
-   La session d’ouverture de session est la même.
-   Le handle d’informations d’identification est le même.

</dd> <dt>

*fContextReq* \[ dans\]
</dt> <dd>

Indicateurs de bits qui indiquent les demandes pour le contexte. Tous les packages ne peuvent pas prendre en charge toutes les exigences. Les indicateurs utilisés pour ce paramètre sont précédés de la \_ demande ISC \_ , par exemple, ISC \_ req \_ Delegate.

Ce paramètre peut être un ou plusieurs des indicateurs d’attributs suivants.



| Valeur                                                                                                                                                                                                                                                                            | Signification                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt>**ISC \_ REQ \_ allouer la \_ mémoire**</dt> <dt>0x100</dt> </dl>                         | Le package de sécurité alloue des tampons de sortie pour l’appelant. Lorsque vous avez fini d’utiliser les tampons de sortie, libérez-les en appelant la fonction [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .<br/>                                                        |
| <span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt>**ISC \_ DEMANDE de \_ connexion**</dt> <dt>0x800</dt> </dl>                                         | Le contexte de sécurité ne gère pas les messages de mise en forme.<br/>                                                                                                                                                                                               |
| <span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt>**ISC \_ \_ \_ Erreur étendue**</dt> de la req <dt>0x4000</dt> </dl>                           | Lorsque des erreurs se produisent, le tiers distant est averti.<br/>                                                                                                                                                                                                   |
| <span id="ISC_REQ_MANUAL_CRED_VALIDATION"></span><span id="isc_req_manual_cred_validation"></span><dl> <dt>**ISC \_ DEMANDE \_ de \_ \_ validation d’cred manuel**</dt> <dt>0x80000</dt> </dl> | Le fournisseur de support de sécurité des informations d’identification (CredSSP) ne doit pas authentifier le serveur automatiquement. Cet indicateur est toujours défini lors de l’utilisation de CredSSP.<br/>                                                                                                              |
| <span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt>**ISC \_ \_ \_ Détection de séquence de demandes**</dt> <dt>0x8</dt> </dl>                           | Détecte les messages reçus en dehors de la séquence.<br/>                                                                                                                                                                                                               |
| <span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt>**ISC \_ \_Flux de demande**</dt> <dt>0x8000</dt> </dl>                                                    | Prend en charge une connexion orientée flux.<br/>                                                                                                                                                                                                                   |
| <span id="ISC_REQ_USE_SUPPLIED_CREDS"></span><span id="isc_req_use_supplied_creds"></span><dl> <dt>**ISC \_ Demandes d’identification \_ \_ fournies \_**</dt> par la req <dt></dt> </dl>                | CredSSP ne doit pas tenter de fournir automatiquement des informations d’identification pour le client.<br/>                                                                                                                                                                            |
| <span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt>**ISC \_ \_Délégué req**</dt> <dt>0x1</dt> </dl>                                                 | Indique que les informations d’identification de l’utilisateur doivent être déléguées au serveur.<br/> Si cet indicateur n’est pas spécifié, un jeu d’informations d’identification vide est délégué au serveur.<br/> **Windows Server 2008 et Windows Vista :** Cet indicateur est obligatoire.<br/> |
| <span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt>**ISC \_ DEMANDE \_ d' \_ authentification mutuelle**</dt> <dt>0X2</dt> </dl>                                       | Indique que l’authentification du serveur n’est pas nécessaire. Les stratégies de délégation sont toujours appliquées si cet indicateur n’est pas spécifié.<br/> **Windows Server 2008 et Windows Vista :** Cet indicateur est ignoré.<br/>                                                 |



 

Les attributs demandés ne sont peut-être pas pris en charge par le client. Pour plus d’informations, consultez le paramètre *pfContextAttr* .

Pour plus d’informations sur les différents attributs, consultez [spécifications de contexte](context-requirements.md).

</dd> <dt>

*Reserved1* \[ dans\]
</dt> <dd>

Réservé. Ce paramètre doit avoir la valeur zéro.

</dd> <dt>

*TargetDataRep* \[ dans\]
</dt> <dd>

Représentation des données, telle que l’ordonnancement des octets, sur la cible. Ce paramètre peut être **Security \_ native \_ DREP** ou **Security \_ Network \_ DREP**.

</dd> <dt>

*pInput* \[ in, out, facultatif\]
</dt> <dd>

Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) qui contient des pointeurs vers les mémoires tampons fournies comme entrée au package. À moins que le contexte client n’ait été initié par le serveur, la valeur de ce paramètre doit être **null** lors du premier appel à la fonction. Lors des appels suivants à la fonction ou lorsque le contexte client a été initié par le serveur, la valeur de ce paramètre est un pointeur vers une mémoire tampon allouée avec suffisamment de mémoire pour contenir le jeton retourné par l’ordinateur distant.

Sur les appels à cette fonction après l’appel initial, il doit y avoir deux mémoires tampons. Le premier a le type **SECBUFFER \_ Token** et contient le jeton reçu du serveur. Le deuxième tampon a le type **SECBUFFER \_ vide**; affectez la valeur zéro aux membres **pvBuffer** et **cbBuffer** .

</dd> <dt>

*Reserved2* \[ dans\]
</dt> <dd>

Réservé. Ce paramètre doit avoir la valeur zéro.

</dd> <dt>

*phNewContext* \[ in, out, facultatif\]
</dt> <dd>

Pointeur vers une structure [CtxtHandle](sspi-handles.md) . Lors du premier appel à **InitializeSecurityContext (CredSSP)**, ce pointeur reçoit le nouveau handle de contexte. Lors du deuxième appel, *phNewContext* peut être le même que le handle spécifié dans le paramètre *phContext* .

Sur les appels après le premier appel, transmettez le handle retourné ici en tant que paramètre *phContext* et spécifiez **null** pour *phNewContext*.

</dd> <dt>

*pOutput* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . Cette structure contient à son tour des pointeurs vers la structure [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) qui reçoit les données de sortie. Si une mémoire tampon a été tapée comme **s \_ ReadWrite** dans l’entrée, elle y figurera à la sortie. Le système alloue une mémoire tampon pour le jeton de sécurité si elle est demandée (par le biais de la **\_ demande ISC \_ allocate \_ Memory**) et remplit l’adresse dans le descripteur de mémoire tampon du jeton de sécurité.

Si l’indicateur de **\_ demande d’allocation de \_ \_ mémoire d’ISC** est spécifié, CredSSP alloue de la mémoire pour la mémoire tampon et place les informations appropriées dans le [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc).

</dd> <dt>

*pfContextAttr* \[ à\]
</dt> <dd>

Pointeur vers un jeu d’indicateurs binaires qui indiquent les [*attributs*](../secgloss/a-gly.md#_security_attribute_gly) du contexte établi. Pour obtenir une description des différents attributs, consultez [spécifications de contexte](context-requirements.md).

Les indicateurs utilisés pour ce paramètre sont préfixés par ISC \_ RET, par exemple **ISC \_ RET \_ Delegate**. Pour obtenir la liste des valeurs valides, consultez le paramètre *fContextReq* .

Ne vérifiez pas les attributs liés à la sécurité jusqu’à ce que l’appel de fonction final soit retourné avec succès. Les indicateurs d’attribut qui ne sont pas liés à la sécurité, tels que l’indicateur **ASC \_ RET \_ allouée la \_ mémoire** , peuvent être vérifiés avant le retour final.

> [!Note]  
> Des attributs de contexte particuliers peuvent changer pendant la négociation avec un homologue distant.

 

</dd> <dt>

*ptsExpiry* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une structure d' [**horodatage**](timestamp.md) qui reçoit l’heure d’expiration du contexte. Il est recommandé que le package de sécurité retourne toujours cette valeur en heure locale. Ce paramètre est facultatif et la **valeur null** doit être transmise pour les clients à courte durée de vie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, elle retourne l’un des codes de réussite suivants.



| Code de retour                                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**s \_ E \_ message incomplet \_**</dt> </dl>     | Les données de l’ensemble du message n’ont pas été lues à partir du câble.<br/> Lorsque cette valeur est retournée, la mémoire tampon *pInput* contient une structure [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) avec un membre **BufferType** de **SecBuffer \_ manquant**. Le membre **cbBuffer** de **SecBuffer** spécifie le nombre d’octets supplémentaires que la fonction doit lire à partir du client avant que cette fonction aboutisse. Même si ce nombre n’est pas toujours exact, son utilisation peut aider à améliorer les performances en évitant les appels multiples à cette fonction.<br/> |
| <dl> <dt>**SEC \_ E \_ OK**</dt> </dl>                      | Le contexte de sécurité a été initialisé avec succès. Il n’est pas nécessaire d’avoir un autre appel [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) . Si la fonction retourne un jeton de sortie, c’est-à-dire si le **\_ jeton SECBUFFER** dans *pOutput* est d’une longueur différente de zéro, ce jeton doit être envoyé au serveur.<br/>                                                                                                   |
| <dl> <dt>**s \_ j’ai \_ terminé \_ et je \_ continue**</dt> </dl> | Le client doit appeler [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) , puis transmettre la sortie au serveur. Le client attend ensuite un jeton retourné et le passe, dans un autre appel, à [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md).<br/>                                                                                                                                                                                                                                            |
| <dl> <dt>**s \_ \_ terminées \_**</dt> </dl>        | Le client doit terminer la génération du message, puis appeler la fonction [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**SEC \_ je \_ continue à avoir \_ besoin**</dt> </dl>        | Le client doit envoyer le jeton de sortie au serveur et attendre un jeton de retour. Le client passe le jeton retourné dans un autre appel à [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md). Le jeton de sortie peut être vide.<br/>                                                                                                                                                                                                                                                              |
| <dl> <dt>**s \_ j’ai des \_ \_ informations d’identification incomplètes**</dt> </dl> | Le serveur a demandé l’authentification du client, mais soit les informations d’identification fournies n’incluent pas de certificat, soit le certificat n’a pas été émis par une autorité de certification approuvée par le serveur. Pour plus d'informations, consultez la section Notes.<br/>                                                                                                                                                                              |



 

Si la fonction échoue, la fonction retourne l’un des codes d’erreur suivants.



| Code de retour                                                                                                          | Description                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**s \_ E \_ mémoire insuffisante \_**</dt> </dl>          | La mémoire disponible est insuffisante pour terminer l’action demandée.<br/>                                                                                                                                                                                                     |
| <dl> <dt>**SEC \_ E \_ \_ erreur interne**</dt> </dl>               | Une erreur qui n’a pas été mappée à un code d’erreur SSPI s’est produite.<br/>                                                                                                                                                                                                                  |
| <dl> <dt>**SEC \_ E \_ handle non valide \_**</dt> </dl>               | Le handle passé à la fonction n’est pas valide.<br/>                                                                                                                                                                                                                            |
| <dl> <dt>**s \_ E \_ jeton non valide \_**</dt> </dl>                | Le jeton d’entrée est incorrect. Les causes possibles incluent un jeton endommagé en transit, un jeton de taille incorrecte et un jeton passé dans le mauvais package de sécurité. Cette dernière condition peut se produire si le client et le serveur n’ont pas négocié le package de sécurité approprié.<br/> |
| <dl> <dt>**s \_ \_ ouverture de session \_ refusée**</dt> </dl>                 | L’ouverture de session a échoué.<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**s \_ E \_ aucune \_ autorité d’authentification \_**</dt> </dl> | Aucune autorité n’a pu être contactée pour l’authentification. Le nom de domaine du tiers d’authentification peut être incorrect, le domaine peut être inaccessible ou une relation d’approbation a peut-être échoué.<br/>                                                                    |
| <dl> <dt>**s \_ E \_ aucune \_ information d’identification**</dt> </dl>               | Aucune information d’identification n’est disponible dans le package de sécurité.<br/>                                                                                                                                    |
| <dl> <dt>**\_cible s \_ E \_ inconnu**</dt> </dl>               | La cible n’a pas été reconnue.<br/>                                                                                                                                                                                                                                             |
| <dl> <dt>**SEC \_ E \_ fonction non prise en charge \_**</dt> </dl>         | La valeur du paramètre *fContextReq* n’est pas valide. Soit un indicateur obligatoire n’a pas été spécifié, soit un indicateur qui n’est pas pris en charge par CredSSP a été spécifié.<br/>                                                                                                                 |
| <dl> <dt>**SEC \_ E \_ \_ principal erroné**</dt> </dl>              | Le principal qui a reçu la demande d’authentification n’est pas le même que celui passé dans le paramètre *pszTargetName* . Cette erreur indique un échec de l’authentification mutuelle.<br/>                                                                                      |
| <dl> <dt>**\_stratégie de \_ délégation \_ E s**</dt> </dl>            | La stratégie ne prend pas en charge la délégation des informations d’identification au serveur cible.<br/>                                                                                                                                                                                                |
| <dl> <dt>**\_NTLM de \_ stratégie sec E \_ \_ uniquement**</dt> </dl>            | La délégation des informations d’identification au serveur cible n’est pas autorisée lorsque l’authentification mutuelle n’est pas effectuée.<br/>                                                                                                                                                                  |
| <dl> <dt>**SEC \_ E \_ échec de l' \_ authentification mutuelle \_**</dt> </dl>          | L’authentification du serveur a échoué lorsque l' \_ \_ indicateur d’authentification mutuelle d’ISC req \_ est spécifié dans le paramètre *fContextReq* .<br/>                                                                                                                                                             |



 

## <a name="remarks"></a>Remarques

L’appelant est chargé de déterminer si les attributs de contexte finaux sont suffisants. Si, par exemple, la confidentialité a été demandée mais n’a pas pu être établie, certaines applications peuvent choisir d’arrêter immédiatement la connexion.

Si les attributs du contexte de sécurité ne sont pas suffisants, le client doit libérer le contexte partiellement créé en appelant la fonction [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) .

Le client appelle la fonction **InitializeSecurityContext (CredSSP)** pour initialiser un contexte sortant.

Pour un contexte de sécurité à deux jambes, la séquence appelante est la suivante :

1.  Le client appelle la fonction avec *phContext* défini sur **null** et remplit le descripteur de mémoire tampon avec le message d’entrée.
2.  Le package de sécurité examine les paramètres et construit un jeton opaque, en le plaçant dans l’élément de jeton dans le tableau de mémoires tampons. Si le paramètre *fContextReq* comprend l’indicateur **ISC \_ req \_ allocate \_ Memory** , le package de sécurité alloue la mémoire et retourne le pointeur dans l’élément de jeton.
3.  Le client envoie le jeton retourné dans la mémoire tampon *pOutput* au serveur cible. Le serveur transmet ensuite le jeton en tant qu’argument d’entrée dans un appel à la fonction [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) .
4.  [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) peut retourner un jeton. Le serveur envoie ce jeton au client par le biais d’un deuxième appel de **InitializeSecurityContext (CredSSP)** si le premier appel a retourné **sec \_ que je \_ continue \_**.

Si le serveur a répondu, le package de sécurité retourne **sec \_ E \_ OK** et une session sécurisée est établie.

Si la fonction retourne l’une des réponses d’erreur, la réponse du serveur n’est pas acceptée et la session n’est pas établie.

Si la fonction retourne **sec \_ i \_ continue \_ needed**, **sec \_ i \_ Completed \_**, ou **sec \_ i \_ Completed \_ et \_ continue**, les étapes 2 et 3 sont répétées.

L’initialisation d’un contexte de sécurité peut nécessiter plusieurs appels à cette fonction, en fonction du mécanisme d’authentification sous-jacent, ainsi que des choix spécifiés dans le paramètre *fContextReq* .

Les paramètres *fContextReq* et *pfContextAttributes* sont des masques de masques qui représentent différents attributs de contexte. Pour obtenir une description des différents attributs, consultez [spécifications de contexte](context-requirements.md). Tandis que le paramètre *pfContextAttributes* est valide en cas de retour correct, vous devez examiner les indicateurs qui se rapportent aux aspects de sécurité du contexte uniquement sur le retour final réussi. Les retours intermédiaires peuvent définir, par exemple, l’indicateur **ISC \_ RET \_ allouée \_ Memory** .

Si l’indicateur d’identification des informations d’identification **\_ \_ \_ \_ fournies** par l’ISC est défini, le package de sécurité doit rechercher un type de tampon **SECBUFFER \_ pkg \_ params** dans la mémoire tampon d’entrée *pInput* . Bien qu’il ne s’agit pas d’une solution générique, elle permet un appariement renforcé du package de sécurité et de l’application, le cas échéant.

Si **la \_ demande ISC \_ allocate \_ Memory** a été spécifiée, l’appelant doit libérer la mémoire en appelant la fonction [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .

Par exemple, le jeton d’entrée peut être le défi d’un gestionnaire de réseau local. Dans ce cas, le jeton de sortie est la réponse chiffrée NTLM à la stimulation.

L’action effectuée par le client dépend du code de retour de cette fonction. Si le code de retour est **sec \_ E \_ OK**, il n’y aura pas d’appel de deuxième **InitializeSecurityContext (CredSSP)** et aucune réponse du serveur ne sera attendue. Si le code de retour est **sec, \_ je \_ continue \_ nécessaire**, le client attend un jeton en réponse du serveur et le transmet dans un deuxième appel à **InitializeSecurityContext (CredSSP)**. Le code de retour de **sec \_ I \_ \_ requis** indique que le client doit terminer la génération du message et appeler la fonction [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) . Les **secondes \_ que j’ai \_ effectuées \_ et qui \_ poursuivent** le code incorporent ces deux actions.

Si **InitializeSecurityContext (CredSSP)** retourne une réussite sur le premier appel (ou uniquement), l’appelant doit finir par appeler la fonction [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) sur le handle retourné, même si l’appel échoue sur une branche ultérieure de l’échange d’authentification.

Le client peut appeler **InitializeSecurityContext (CredSSP)** une fois qu’il s’est terminé avec succès. Cela indique au package de sécurité qu’une réauthentification est souhaitée.

Les appelants en mode noyau présentent les différences suivantes : le nom cible est une chaîne [*Unicode*](../secgloss/u-gly.md#_security_unicode_gly) qui doit être allouée dans la mémoire virtuelle à l’aide de [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc); elle ne doit pas être allouée à partir du pool. Les mémoires tampons transmises et fournies dans *pInput* et *pOutput* doivent être dans la mémoire virtuelle, et non dans le pool.

Si la fonction retourne **les \_ \_ \_ informations d’identification s I incomplètes**, vérifiez que les informations d’identification r transmises à la fonction [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) spécifiaient un certificat valide et approuvé. le certificat doit être un certificat d’authentification client émis par une autorité de certification approuvée par le serveur. Pour obtenir une liste des autorités de certification approuvées par le serveur, appelez la fonction [**QueryContextAttributes (CredSSP)**](querycontextattributes--credssp.md) avec la **liste d' \_ émetteurs SECPKG attr \_ \_ \_ ex** Attribute.

Après avoir reçu un certificat d’authentification d’une autorité de certification approuvée par le serveur, l’application cliente crée de nouvelles informations d’identification. Pour ce faire, il appelle la fonction [**CredSSP (AcquireCredentialsHandle)**](acquirecredentialshandle--credssp.md) , puis l’appel de **InitializeSecurityContext (CredSSP)** , en spécifiant les nouvelles informations d’identification dans le paramètre *phCredential* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>SSPI. h (include Security. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md)
</dt> <dt>

[**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md)
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

 

 
