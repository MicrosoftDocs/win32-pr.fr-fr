---
description: Définit le type de points de terminaison qui peuvent être utilisés pour se connecter à un service.
ms.assetid: 50397D25-7C71-4AA2-89BF-F90CBDCFFA91
title: Énumération UpdateEndpointType (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: 7fbfd67b3009fbe904284ea7a92cdea996d0a6e23a43a17639eb567d66536917
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462909"
---
# <a name="updateendpointtype-enumeration"></a>Énumération UpdateEndpointType

Définit le type de points de terminaison qui peuvent être utilisés pour se connecter à un service.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagEndpointType { 
  uetClientServer          = 0,
  uetReporting             = ( uetClientServer + 1 ),
  uetWuaSelfUpdate         = ( uetReporting + 1 ),
  uetRegulation            = ( uetWuaSelfUpdate + 1 ),
  uetSimpleTargeting       = ( uetRegulation + 1 ),
  uetSecuredClientServer   = ( uetSimpleTargeting + 1 ),
  uetSecondaryServiceAuth  = ( uetSecuredClientServer + 1 )
} UpdateEndpointType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**
</dt> <dd>

point de terminaison client-serveur utilisé pour se connecter au service de mise à jour, tel que Windows Update, Microsoft Update et serveur WSUS dans un environnement d’entreprise, pour rechercher des informations sur les mises à jour qui peuvent s’appliquer à l’ordinateur.

Le service de mise à jour retourne des informations sur les mises à jour qui ont été publiées, révisées ou retirées depuis la dernière synchronisation avec le serveur par le client.

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**
</dt> <dd>

Point de terminaison de création de rapports utilisé lorsque le client signale les résultats des analyses, des téléchargements et des réinstallations dans le service de mise à jour.

dans le cas des services publics (Windows Update et Microsoft Update), cette opération est effectuée à des fins de surveillance de la qualité.

Dans le cas de services privés, tels qu’un serveur WSUS d’entreprise, le type de point de terminaison thhis permet également au serveur de collecter l’inventaire et d’autres informations sur les ordinateurs clients sous gestion.

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**
</dt> <dd>

point de terminaison à mise à jour automatique qui est utilisé lorsque l’ordinateur client contacte un service de mise à jour pour déterminer s’il existe une nouvelle version du logiciel client de l’Agent Windows Update.

Le point de terminaison de mise à jour automatique utilise un protocole différent, puis le point de terminaison Client-Server pour que les mises à jour automatiques puissent être distribuées même en cas de condition d’erreur susceptible d’empêcher la synchronisation client-serveur normale de fonctionner sur un ordinateur client particulier.

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**
</dt> <dd>

Point de terminaison de réglementation utilisé lorsque l’ordinateur client contacte le service de régulation pour agir sur une mise à jour particulière applicable à l’ordinateur cible.

Le service de régulation peut indiquer si la mise à jour est « réglementée » (également appelée « limitation »). en d’autres termes, le service de régulation peut indiquer à l’ordinateur client qu’il ne doit pas agir sur une mise à jour particulière, même si cette mise à jour s’applique.

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**
</dt> <dd>

Point de terminaison de ciblage simple utilisé uniquement avec les services privés (serveurs WSUS dans les environnements d’entreprise). Dans un environnement d’entreprise, les ordinateurs clients peuvent être attribués à des groupes cibles particuliers et les mises à jour peuvent être installées sur les ordinateurs de certains groupes, mais pas sur d’autres.

Par exemple, l’administrateur WSUS peut créer un groupe de « test » pour les ordinateurs utilisés pour tester les nouvelles mises à jour, et l’administrateur peut approuver les mises à jour nouvellement publiées à installer sur les ordinateurs du groupe de test sans les approuver pour l’installation sur d’autres ordinateurs de l’organisation. Le simple ciblage d’Exchange est utilisé pour permettre à un ordinateur client de s’inscrire auprès du serveur WSUS et d’autoriser le serveur à indiquer à l’ordinateur client le groupe dans lequel il se trouve.

</dd> <dt>

<span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetSecuredClientServer**
</dt> <dd>

Point de terminaison sécurisé client-serveur qui permet à un client d’obtenir des informations sur les applications qui ont besoin d’une licence pour pouvoir les utiliser sur un ordinateur client. cette infrastructure de licences est actuellement utilisée uniquement par Windows 8 pour déployer des applications et des mises à jour obtenues via le Windows Store. le point de terminaison sécurisé-client-serveur n’est actuellement pas utilisé par Windows Update, Microsoft Update ou WSUS.

</dd> <dt>

<span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetSecondaryServiceAuth**
</dt> <dd>

Le point de terminaison d’authentification de service secondaire est utilisé par un client pour fournir l’authentification avant d’obtenir des informations sur les applications qui ont besoin d’une licence pour pouvoir les utiliser sur un ordinateur client. cette infrastructure de licences est actuellement utilisée uniquement par Windows 8 pour déployer des applications et des mises à jour obtenues via le Windows Store. le point de terminaison d’authentification de service secondaire n’est actuellement pas utilisé par Windows Update, Microsoft Update ou WSUS.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                              |
| En-tête<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |



 

 




