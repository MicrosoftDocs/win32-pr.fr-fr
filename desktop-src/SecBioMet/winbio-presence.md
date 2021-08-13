---
title: Structure WINBIO_PRESENCE ( \_ types WINBIO. h)
description: Contient des informations sur la présence d’une personne dont la présence est surveillée.
ms.assetid: 810D452E-DDFA-4AB2-AEFB-0C170C0C18D4
keywords:
- API de Windows Biometric Framework de structure de WINBIO_PRESENCE
- API du pointeur de structure PWINBIO_PRESENCE Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2671faaee7bc277f9389d7c993e4d511dac03db459755b40bf3f659ff5256a56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909577"
---
# <a name="winbio_presence-structure"></a>\_Structure de présence WINBIO

Contient des informations sur la présence d’une personne dont la présence est surveillée.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WINBIO_PRESENCE {
  WINBIO_BIOMETRIC_TYPE      Factor;
  WINBIO_BIOMETRIC_SUBTYPE   SubFactor;
  HRESULT                    Status;
  WINBIO_REJECT_DETAIL       RejectDetail;
  WINBIO_IDENTITY            Identity;
  ULONGLONG                  TrackingId;
  WINBIO_PROTECTION_TICKET   Ticket;
  WINBIO_PRESENCE_PROPERTIES Properties;
} WINBIO_PRESENCE, *PWINBIO_PRESENCE;
```



## <a name="members"></a>Membres

<dl> <dt>

**Facteur**
</dt> <dd>

Facteur biométrique utilisé pour surveiller la présence de la personne.

</dd> <dt>

**Sous-fait**
</dt> <dd>

Qualificateur du sous-fait biométrique pour le facteur biométrique utilisé pour surveiller la présence de l’individu.

</dd> <dt>

**État**
</dt> <dd>

État de la procédure d’identification pour la personne.

</dd> <dt>

**RejectDetail**
</dt> <dd>

Informations supplémentaires sur l’échec de la reconnaissance d’un individu, y compris des commentaires qui expliquent comment corriger l’erreur.

</dd> <dt>

**Identité**
</dt> <dd>

Identité de la personne dont la présence est surveillée, une fois que cette personne a été identifiée.

</dd> <dt>

**TrackingId**
</dt> <dd>

Entier qui est généré par l’adaptateur et identifie de façon unique l’individu. L’identificateur de suivi que l’adaptateur affecte à un individu particulier est garanti comme étant constant tant que cette personne reste dans le cadre de l’appareil photo.

</dd> <dt>

**Ticket**
</dt> <dd>

Réservé. Attribuez la valeur 0 à l’adaptateur.

</dd> <dt>

**Propriétés**
</dt> <dd>

Informations spécifiques au facteur sur la position d’un individu.

</dd> </dl>

## <a name="remarks"></a>Remarques

La fonction [**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) crée un tableau de structures de **\_ présence WINBIO** et envoie ce tableau au service biométrique. Le service biométrique utilise le tableau pour mettre à jour son modèle interne d’êtres humains près de l’ordinateur.

Selon les résultats de cette mise à jour, le service biométrique peut générer une structure de [**\_ \_ Résultat asynchrone WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) pour la fonction [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence) pour tous les clients avec des moniteurs de présence actifs. **\_ Résultat asynchrone WINBIO \_ .** Le membre Operation de la structure contient la **\_ présence du \_ moniteur \_ d’opération WINBIO** et le **\_ Résultat asynchrone WINBIO \_ . Le membre Parameters. MonitorPresence. ChangeType** fournit des informations supplémentaires sur l’état de la personne.

Lorsqu’un individu que l’adaptateur de moteur associe à un identificateur de suivi particulier apparaît dans le flux d’entrée pour la première fois, le service biométrique génère une structure de [**\_ \_ Résultat asynchrone WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) côté client où le **\_ Résultat asynchrone WINBIO \_ . Le membre Parameters. MonitorPresence. ChangeType** est **WINBIO \_ type de modification \_ \_ arrivée**. Cette structure est envoyée à votre fonction de rappel d’application ou à la file d’attente de messages d’application avant toute autre structure de **\_ \_ Résultat asynchrone WINBIO** où le **\_ Résultat asynchrone WINBIO \_ . Parameters. MonitorPresence. PresenceArray** comprend une structure de **\_ présence WINBIO** avec la même valeur pour la **\_ présence WINBIO. TrackingId**.

Les combinaisons de valeurs suivantes dans le tableau de structures de **\_ présence WINBIO** que **le \_ Résultat asynchrone WINBIO \_ . Le membre Parameters. MonitorPresence. PresenceArray** indique des genres spécifiques de modifications de l’état d’un individu.

-   Lorsqu’un individu est visible dans le cadre de l’appareil photo, mais que le moteur essaie toujours d’identifier l’individu, les membres de la structure de **\_ présence WINBIO** ont les valeurs dans le tableau suivant.

    

    | Membre            | Valeur                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | Entier qui identifie le individuel au moteur. |
    | **État**        | **\_OK**                                                |
    | **Identity. type** | **\_type d’ID WINBIO \_ \_ null**                               |

    

     

    Dans ce cas, le service biométrique étend le délai d’expiration pour l’individu et ne génère pas de structure de [**\_ \_ résultat WINBIO Async**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) côté client pour l’identificateur de suivi où le **\_ Résultat asynchrone WINBIO \_ . Le membre Parameters. MonitorPresence. ChangeType** est **WINBIO \_ type de modification \_ \_ Recognize**.

    La première fois qu’une structure de [**\_ \_ Résultat asynchrone WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) inclut une structure de **\_ présence WINBIO** où le membre **Status** est **\_ OK** et que le membre **Identity. type** est **WINBIO \_ type d’ID \_ \_ null** après qu’une ou plusieurs structures de **\_ \_ résultats asynchrones WINBIO** ont inclus **une structure de \_ \_** **\_ présence WINBIO** avec un membre **Status** de **WINBIO \_ E \_ Bad \_ capture** **\_ \_ Le membre Parameters. MonitorPresence. ChangeType** est **WINBIO \_ \_ type change \_ Track**. Cette structure de **\_ \_ résultat WINBIO Async** où **WINBIO est le \_ \_ Résultat asynchrone. Le membre Parameters. MonitorPresence. ChangeType** est **WINBIO \_ \_ type \_ de modification** informe le client que le problème à l’origine de l’erreur de **\_ \_ \_ capture incorrecte de WINBIO E** a été résolu. Pour plus d’informations sur les circonstances dans lesquelles une structure de **\_ présence WINBIO** a un membre **Status** de **WINBIO \_ E \_ Bad \_ capture**, consultez la description de la manière dont l’adaptateur de moteur fournit des commentaires à l’utilisateur pour corriger les échecs de reconnaissance plus loin dans ces notes.

-   Lorsqu’un individu est visible dans le cadre de l’appareil photo, mais que le moteur essaie toujours d’identifier l’individu et souhaite fournir des commentaires à l’utilisateur sur la manière de corriger un échec de reconnaissance, les membres de la structure de **\_ présence WINBIO** ont les valeurs dans le tableau suivant.

    

    | Membre                                                                                                      | Valeur                                                                         |
    |-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
    | **TrackingId**                                                                                              | Entier qui identifie le individuel au moteur.                      |
    | **État**                                                                                                  | **WINBIO \_ E \_ mauvaise \_ capture**                                                   |
    | **Identity. type**                                                                                           | **\_type d’ID WINBIO \_ \_ null**                                                    |
    | **Properties. FacialFeatures. BoundingBox**, si la valeur de **Factor** est **WINBIO \_ , \_ tapez \_ caractéristiques du visage** | Emplacement de la face du individu dans le cadre de l’appareil photo.           |
    | **Properties. iris. BoundingBox**, si la valeur de **Factor** est **WINBIO \_ type \_ Iris**                       | Emplacement du diaphragme ou de la Irises de l’individu dans le cadre de l’appareil photo. |

    

     

    Dans ce cas, le service biométrique étend l’heure d’expiration pour la personne et génère une structure [**de \_ \_ Résultat asynchrone WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) pour l’identificateur de suivi où le **\_ Résultat asynchrone WINBIO \_ . Le membre Parameters. MonitorPresence. ChangeType** est **WINBIO \_ \_ type change \_ Track**.

-   Lorsqu’un individu est visible dans le cadre de l’appareil photo et que l’adaptateur du moteur détermine l’identité de la personne, les membres de la structure de **\_ présence WINBIO** ont les valeurs dans le tableau suivant.

    

    | Membre                        | Valeur                                                    |
    |-------------------------------|----------------------------------------------------------|
    | **TrackingId**                | Entier qui identifie le individuel au moteur. |
    | **État**                    | **\_OK**                                                |
    | **Identity. type**             | **\_ID \_ sid type \_ WINBIO**                                |
    | **Identity. Value. AccountSid** | Identificateur de sécurité (SID) de la personne.         |

    

     

    Dans ce cas, le service biométrique associe l’identificateur de suivi au SID pour la personne et génère une structure de [**résultat WINBIO \_ Async \_**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) côté client pour l’identificateur de suivi où le **\_ Résultat asynchrone WINBIO \_ . Le membre Parameters. MonitorPresence. ChangeType** est **WINBIO \_ type de modification \_ \_ Recognize**. Le service biométrique ne génère pas de structures de **\_ \_ Résultat asynchrone WINBIO** côté client supplémentaires pour l’identificateur de suivi, sauf si l’individu quitte le cadre de l’appareil photo.

-   Lorsqu’un individu est visible dans le cadre de l’appareil photo, mais que l’adaptateur du moteur détermine que l’individu n’est pas inscrit, les membres de la structure de **\_ présence WINBIO** ont les valeurs dans le tableau suivant.

    

    | Membre            | Valeur                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | Entier qui identifie le individuel au moteur. |
    | **État**        | **WINBIO \_ E \_ \_ ID inconnu**                               |
    | **Identity. type** | **\_type d’ID WINBIO \_ \_ null**                               |

    

     

    Dans ce cas, le service biométrique associe l’identificateur de suivi de la personne avec une identité inconnue, et génère une structure de [**résultat WINBIO \_ Async \_**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) côté client pour l’identificateur de suivi où le **\_ Résultat asynchrone WINBIO \_ . Le membre Parameters. MonitorPresence. ChangeType** est **WINBIO \_ type de modification \_ \_ Recognize**. Le service biométrique ne génère pas de structures de **\_ \_ Résultat asynchrone WINBIO** côté client supplémentaires pour l’identificateur de suivi, sauf si l’individu quitte le cadre de l’appareil photo.

Lorsqu’un individu que l’adaptateur de moteur associe à un identificateur de suivi particulier quitte le frame de l’appareil photo et cesse d’apparaître dans les valeurs renvoyées par la fonction [**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) , l’identificateur de suivi finit par expirer. Lorsque l’identificateur de suivi expire, le service biométrique génère une structure de [**\_ \_ Résultat asynchrone WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) côté client où le **\_ Résultat asynchrone WINBIO \_ . Le membre Parameters. MonitorPresence. ChangeType** est **WINBIO \_ type de modification \_ \_**. L’adaptateur de moteur peut empêcher le service biométrique de générer cette structure avec la valeur de l' **élément de \_ modification de \_ type \_ WINBIO** en incluant une structure de **\_ présence WINBIO** dans le tableau retourné par **EngineAdapterIdentifyAll** , où la **\_ présence WINBIO.** Le membre d’État est **S \_ OK** et la **\_ présence WINBIO. Le membre Identity. type** est un **WINBIO d’ID de \_ \_ type \_ null** , comme décrit précédemment dans ces remarques. Cette action prolonge l’heure d’expiration pour l’identificateur de suivi sans entraîner d’activité côté client.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                                                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                                                                                                     |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Résultat asynchrone \_ WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence)
</dt> <dt>

[**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn)
</dt> </dl>

 

 





