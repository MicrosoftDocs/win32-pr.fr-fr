---
description: Les termes suivants sont utiles pour comprendre la technologie TAPI.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 36b1d6c3-2d57-4b38-a35f-6bf632411c6e
title: T (API de téléphonie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fef6d897365042552429cc7679363c2e23152cef6492dfc84f25b6b32fb7a99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518399"
---
# <a name="t-telephony-api"></a>T (API de téléphonie)

[A](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [e](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) T [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z

<dl> <dt>

<span id="tapi2.t1_e1_tapgloss"></span><span id="TAPI2.T1_E1_TAPGLOSS"></span>**T1/E1**
</dt> <dd>

Un lien de transmission numérique avec une capacité de 1 544 Mbits/s. Aux États-Unis, ce lien est appelé *T1*. Dans l’Union européenne, il est appelé *E1*. Voir [*mégabits par seconde (Mbits/s)*](m-tapgloss.md).

</dd> <dt>

<span id="tapi2.tapi_tapgloss"></span><span id="TAPI2.TAPI_TAPGLOSS"></span>**TÉLÉPHONIE**
</dt> <dd>

Voir *interface de programmation d’applications de téléphonie (TAPI)*.

</dd> <dt>

<span id="tapi2.tapisrv_tapgloss"></span><span id="TAPI2.TAPISRV_TAPGLOSS"></span>**tapisrv**
</dt> <dd>

Application de service de prise en charge qui fournit un contexte d’exécution pour la bibliothèque de liens dynamiques TAPI afin d’effectuer des tâches telles que l’allocation de mémoire ou l’accès aux structures de données qui ont été échangées sur le disque.

</dd> <dt>

<span id="tapi2.tdd_tapgloss"></span><span id="TAPI2.TDD_TAPGLOSS"></span>**PILOTÉ**
</dt> <dd>

Consultez *appareils de télécommunications pour les sourds (TDD)*.

</dd> <dt>

<span id="tapi2.telecommucations_devices_for_the_deaf_tdd__tapgloss"></span><span id="TAPI2.TELECOMMUCATIONS_DEVICES_FOR_THE_DEAF_TDD__TAPGLOSS"></span>**Appareils Telecommucations pour les sourds (TDD)**
</dt> <dd>

Périphérique de données pour la transmission de signaux codés. En règle générale, l’appareil est un simple terminal informatique constitué d’un clavier, d’un coupleur acoustique et d’un écran, et s’exécute à 300 bauds.

</dd> <dt>

<span id="tapi2.telephony_tapgloss"></span><span id="TAPI2.TELEPHONY_TAPGLOSS"></span>**téléphonie**
</dt> <dd>

La science de la transmission de signaux vocaux, de données, de vidéos ou d’images sur une distance à l’aide de la technologie qui intègre les ordinateurs au réseau téléphonique.

</dd> <dt>

<span id="tapi2.telephony_application_programming_interface_tapi__tapgloss"></span><span id="TAPI2.TELEPHONY_APPLICATION_PROGRAMMING_INTERFACE_TAPI__TAPGLOSS"></span>**Interface de programmation d’applications de téléphonie (TAPI)**
</dt> <dd>

Ensemble de fonctions qui permettent de programmer des appareils basés sur des lignes téléphoniques de manière indépendante du périphérique, en fournissant une téléphonie personnelle aux utilisateurs. L’interface TAPI prend en charge la transmission vocale et de données, autorise un large éventail de périphériques terminaux et prend en charge des types de connexion et des techniques de gestion des appels complexes, tels que les conférences téléphoniques, les appels en attente et la messagerie vocale. L’interface TAPI autorise tous les éléments de l’utilisation téléphonique, de l’appel simple entre la numérotation et la parole à la messagerie électronique internationale, à être contrôlé dans les applications développées pour Microsoft Windows. Consultez la [vue d’ensemble de la téléphonie Microsoft](./microsoft-telephony-overview.md)

</dd> <dt>

<span id="tapi2.telephony_service_provider_interface_tspi__tapgloss"></span><span id="TAPI2.TELEPHONY_SERVICE_PROVIDER_INTERFACE_TSPI__TAPGLOSS"></span>**Interface du fournisseur de services de téléphonie (TSPI)**
</dt> <dd>

outil de création de fournisseurs de services pour les systèmes d’exploitation Microsoft Windows. TSPI définit la manière dont le réseau partage des informations avec Windows téléphonie, qui à son tour communique avec l’API, qui communique avec les applications de téléphonie Windows. Pour plus d’informations, consultez [TSPI (Telephony Service Provider Interface)](./telephony-service-provider-interface-tspi-.md).

</dd> <dt>

<span id="tapi2.third_party_call_control_tapgloss"></span><span id="TAPI2.THIRD_PARTY_CALL_CONTROL_TAPGLOSS"></span>**contrôle des appels tiers**
</dt> <dd>

Un modèle de contrôle d’appel du tiers qui permet à une application d’établir ou de répondre à un appel entre deux parties.

</dd> <dt>

<span id="tapi2.time_to_live_ttl__tapgloss"></span><span id="TAPI2.TIME_TO_LIVE_TTL__TAPGLOSS"></span>**durée de vie (TTL)**
</dt> <dd>

Valeur comprise entre 0 et 255 qui définit l’étendue au sein de laquelle les paquets de multidiffusion doivent être envoyés sur un réseau à l’aide du protocole IP (Internet Protocol). L’étendue est définie en termes de la façon dont la destination d’un paquet local ou distant est. Chaque routeur décrémente la durée de vie d’une unité. Lorsque la valeur atteint une limite inférieure prédéfinie, le routeur rejette le paquet. Les exigences actuelles de la multidiffusion (MBONE), disponibles sur le site faq.txt ftp://ftp.isi.edu/mbone/, définissent les étendues standard suivantes : réseau local, 1 ; site local, 15 ; région, 63 ; monde, 127. D’autres paramètres peuvent avoir une signification locale ; par exemple, 31 peut indiquer tous les sites d’une organisation particulière.

</dd> <dt>

<span id="tapi2.tspi_tapgloss"></span><span id="TAPI2.TSPI_TAPGLOSS"></span>**TSPI**
</dt> <dd>

Voir [interface du fournisseur de services de téléphonie (TSPI)](./telephony-service-provider-interface-tspi-.md).

</dd> <dt>

<span id="tapi2.ttl_tapgloss"></span><span id="TAPI2.TTL_TAPGLOSS"></span>**EXPIRATION**
</dt> <dd>

Consultez *durée de vie (TTL)*.

</dd> <dt>

<span id="tapi2.twisted_pair_tapgloss"></span><span id="TAPI2.TWISTED_PAIR_TAPGLOSS"></span>**paire torsadée**
</dt> <dd>

Câblage téléphonique normal. Chaque câble téléphonique est en fait une paire de fils.

</dd> </dl>

 

 
