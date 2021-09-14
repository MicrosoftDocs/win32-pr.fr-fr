---
description: Les termes suivants sont utiles pour comprendre la technologie TAPI.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b4256a4a-c19e-4431-b62f-9e9fef4b5827
title: S (API de téléphonie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f33f4d2c16110ad6c79a02401c6a63ad0fb8f4f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414684"
---
# <a name="s-telephony-api"></a>S (API de téléphonie)

[A](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [e](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) S [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z

<dl> <dt>

<span id="tapi2.service_provider_tapgloss"></span><span id="TAPI2.SERVICE_PROVIDER_TAPGLOSS"></span>**fournisseur de services**
</dt> <dd>

Bibliothèque de liens dynamiques qui prend en charge les communications sur un réseau téléphonique via un ensemble de fonctions de service exportées. Le fournisseur de services répond aux demandes de téléphonie, qui lui sont envoyées par la bibliothèque de liens dynamiques TAPI, en effectuant les tâches de bas niveau nécessaires pour communiquer sur le réseau téléphonique. De cette façon, le fournisseur de services, en association avec l’interface TAPI, protège les applications des détails liés aux services et à la technologie de la communication du réseau téléphonique.

</dd> <dt>

<span id="tapi2.subaddressing_tapgloss"></span><span id="TAPI2.SUBADDRESSING_TAPGLOSS"></span>**sous-adressage**
</dt> <dd>

Fonctionnalité fournie sur les lignes RNIS, qui permet d’obtenir plus d’informations qu’un simple numéro de téléphone à utiliser lors de la numérotation.

</dd> <dt>

<span id="tapi2.supplementary_telephony_tapgloss"></span><span id="TAPI2.SUPPLEMENTARY_TELEPHONY_TAPGLOSS"></span>**Téléphonie supplémentaire**
</dt> <dd>

Niveau de service qui fournit des fonctionnalités de commutateur avancées, telles que le maintien, le transfert, etc. Tous les services supplémentaires sont facultatifs. autrement dit, le fournisseur de services n’est pas tenu de les prendre en charge. Consultez [*téléphonie assistée*](a-tapgloss.md), [*téléphonie de base*](b-tapgloss.md), [*téléphonie étendue*](e-tapgloss.md#tapi2.extended_telephony_tapgloss).

</dd> <dt>

<span id="tapi2.switched_56_tapgloss"></span><span id="TAPI2.SWITCHED_56_TAPGLOSS"></span>**Commuté 56**
</dt> <dd>

Service de données commuté qui permet à l’utilisateur de composer une autre personne et de transmettre en duplex intégral, Digital Synchronous 56 Kbps pour le prix d’un appel téléphonique.

</dd> <dt>

<span id="tapi2.synchronous_tapgloss"></span><span id="TAPI2.SYNCHRONOUS_TAPGLOSS"></span>**synchronise**
</dt> <dd>

Méthode de transmission de données dans laquelle il existe un temps constant entre les bits, les caractères ou les événements successifs. Le minutage est atteint par le partage d’une seule horloge. Chaque fin de la transmission se synchronise avec l’utilisation des horloges et des informations envoyées avec les données transmises. Les caractères sont espacés par heure, et non pas par les bits de démarrage et d’arrêt. Voir [*asynchrone*](a-tapgloss.md).

</dd> </dl>

 

 



