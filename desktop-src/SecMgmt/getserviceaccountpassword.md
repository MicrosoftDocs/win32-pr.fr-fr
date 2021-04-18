---
description: Récupère le mot de passe du compte de service.
ms.assetid: B3D3842F-ACEB-4979-B336-BA3D0143044C
title: GetServiceAccountPassword, fonction (Secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetServiceAccountPassword
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 08719fb2b7e4a775df890f20cd640d059cb44475
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520053"
---
# <a name="getserviceaccountpassword-function"></a>GetServiceAccountPassword fonction)

Récupère le mot de passe du compte de service, disponible pour les [*fournisseurs de support de sécurité*](/windows/desktop/SecGloss/s-gly) (SSP), tels que Kerberos ssp.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS NTAPI GetServiceAccountPassword(
  _In_        PUNICODE_STRING AccountName,
  _In_opt_    PUNICODE_STRING DomainName,
  _In_        CRED_FETCH      CredFetch,
  _Inout_opt_ FILETIME        *FileTimeExpiry,
  _Out_       PUNICODE_STRING CurrentPassword,
  _Out_       PUNICODE_STRING PreviousPassword,
  _Out_opt_   FILETIME        *FileTimeCurrPwdValidForOutbound
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AccountName* \[ dans\]
</dt> <dd>

Nom de compte terminé par le caractère null du compte de service administré de groupe (gMSA). Le nom d’utilisateur peut prendre l’une des formes suivantes :

-   Nom de compte SAM du gMSA.
-   Nom d’utilisateur dans un nom de domaine complet (FQDN), tel que *nom_domaine * **\\** _NomUtilisateur_ ou **www.** _domaine_* _. com \\_ * _nom_. Le nom d’utilisateur doit être un nom SAM uniquement. Le nom de domaine peut être un nom DNS ou un nom NetBIOS.
-   Nom d’utilisateur principal (UPN) implicite pour le compte gMSA, par exemple, *nom * **@** _domaine_*_. com_* où, en fonction de la définition d’un UPN implicite, le *domaine * * *. com** est le nom DNS de domaine réel.

</dd> <dt>

*Nom_domaine* \[ dans, facultatif\]
</dt> <dd>

Nom de domaine se terminant par un caractère null facultatif. Cela n’est valide que si le paramètre *AccountName* est un nom de compte Sam. Le nom de domaine ne peut être qu’un nom NetBIOS ou un nom de domaine complet (FQDN).

</dd> <dt>

*CredFetch* \[ dans\]
</dt> <dd>

Valeur de l’énumération d' [**\_ extraction de cred**](cred-fetch.md) qui spécifie comment récupérer les informations d’identification.



| Valeur                                                                                                                                                                                                    | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span><dl> <dt>**CredFetchDefault**</dt> </dl> | Le système d’exploitation tente d’abord de récupérer le mot de passe à partir du cache local s’il n’est pas nécessaire d’extraire le mot de passe. S’il est temps de récupérer le mot de passe, le système d’exploitation contacte le contrôleur de domaine, sinon, retourne tous les mots de passe mis en cache dont la valeur d’État est Success.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span><dl> <dt>**CredFetchDPAPI**</dt> </dl>         | Retourne les informations d’identification DPAPI locales à l’appelant. Les SSP n’ont généralement pas besoin d’utiliser cette valeur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span><dl> <dt>**CredFetchForced**</dt> </dl>     | Force le système d’exploitation à tenter de lire le mot de passe à partir du contrôleur de domaine. Pendant l’heure de substitution du mot de passe, le mot de passe peut avoir changé au niveau du contrôleur de domaine et d’autres hôtes membres, mais l’hôte du membre gMSA reconnaît le mot de passe comme étant toujours valide. Cela peut se produire en raison de problèmes d’inclinaison de l’horloge entre les différents contrôleurs de domaine. Lorsque cette valeur est spécifiée, le système d’exploitation détermine s’il peut y avoir une possibilité de modification de mot de passe en raison de l’inclinaison de l’horloge et, le cas échéant, récupère le mot de passe. Dans le cas contraire, les informations d’identification mises en cache sont retournées. S’il n’y a pas d’informations d’identification mises en cache, le système d’exploitation tente d’en récupérer un à partir du contrôleur de domaine.<br/> |



 

</dd> <dt>

*FileTimeExpiry* \[ in, out, facultatif\]
</dt> <dd>

En entrée, si cette valeur n’est pas null et n’est pas un **fileTime** zéro, *FileTimeExpiry* contient l’heure d’expiration des informations d’identification du compte de service, comme l’appelant l’appelle. Si le paramètre *FileTimeExpiry* est identique à l’une des informations d’identification actuelles, cet appel échoue. Lors de la sortie, le paramètre *FileTimeExpiry* contient l’heure d’expiration des informations d’identification retournées.

</dd> <dt>

*CurrentPassword* \[ à\]
</dt> <dd>

Mot de passe actuel du gMSA.

</dd> <dt>

*PreviousPassword* \[ à\]
</dt> <dd>

Mot de passe précédent de gMSA.

</dd> <dt>

*FileTimeCurrPwdValidForOutbound* \[ out, facultatif\]
</dt> <dd>

Indique l’heure après laquelle le mot de passe actuel est valide pour les demandes sortantes. L’appelant doit comparer l’heure actuelle avec cette valeur et utiliser le mot de passe actuel retourné uniquement si l’heure actuelle est supérieure ou égale à la valeur retournée par ce paramètre. L’utilisation de ce paramètre est conçue pour les appelants qui n’ont pas de nouvelle tentative dans la logique sortante, par exemple, NTLM.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est STATUs \_ successful.

Si la fonction échoue, la valeur de retour est un code NTSTATUS. Pour plus d’informations, consultez valeurs de retour de la [fonction de stratégie LSA](management-return-values.md).

Vous pouvez utiliser la fonction [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) pour convertir le code NTSTATUS en code d’erreur Windows.

Lorsque vous avez terminé d’utiliser les mémoires tampons retournées dans les paramètres *CurrentPassword* et *PreviousPassword* , libérez-les en appelant la fonction [**FreeLsaHeap**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap) .

## <a name="remarks"></a>Notes

La fonction **GetServiceAccountPassword** peut être appelée dans les scénarios suivants :

-   À partir des fonctions d’ouverture de session des fournisseurs SSP (Security Support Provider), le SSP doit détecter que le \_ mot de passe du compte de service \_ est utilisé pour se connecter à l’entité et doit vérifier que l’appelant possède un privilège TCB ou est un service réseau. Ensuite, le SSP doit autoriser le processus de connexion à continuer en obtenant les informations d’identification les plus récentes en appelant la fonction **GetServiceAccountPassword** avec la valeur **CredFetchDefault** dans l’énumération [**\_ Fetch FETCH**](cred-fetch.md) .

-   Des SSP dans leurs appels [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) et [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) . Les SSP doivent détecter que le \_ \_ mot de passe du compte de service est utilisé pour ces appels, et si l’appel concerne les informations d’identification non principales, le SSP doit s’assurer que l’appelant possède un privilège TCB ou est un service réseau. Le SSP doit ensuite appeler la fonction **GetServiceAccountPassword** avec la valeur **CredFetchDefault** dans l’énumération d' [**\_ extraction cred**](cred-fetch.md) et procéder à l’appel. Si les appels **InitializeSecurityContext** et **AcceptSecurityContext** échouent, le SSP doit utiliser le *FileTimeExpiry* récupéré à partir de l’appel précédent à **GetServiceAccountPassword** et l’utiliser comme entrée pour appeler à nouveau **GetServiceAccountPassword** à l’aide de la valeur **CredFetchForced** dans l’énumération **\_ Fetch FETCH** . Si de nouvelles informations d’identification gMSA sont disponibles, le deuxième appel sera correctement effectué avec les nouvelles informations d’identification et le SSP devra ensuite réessayer avec les nouvelles informations d’identification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Secpkg. h</dt> </dl> |



 

