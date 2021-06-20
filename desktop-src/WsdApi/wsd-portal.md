---
description: En savoir plus sur l’implémentation de WSD (Web Services on Devices). Comprenez son objectif, où il s’applique, l’audience du développeur et les exigences d’exécution.
ms.assetid: 590e0b0b-763c-44fb-a49f-606415f57b26
title: Services Web sur les appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 267f8dba0fd56c383dd3cecabb3c00959aa0d90c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405752"
---
# <a name="web-services-on-devices"></a>Services Web sur les appareils

## <a name="purpose"></a>Objectif

L’API Microsoft Web Services on Devices (WSDAPI) prend en charge l’implémentation d’appareils et de services contrôlés par le client, ainsi que les hôtes d’appareils conformes au [profil des appareils pour les services Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). WSDAPI utilise [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) pour la découverte des appareils.

WSDAPI peut être utilisé pour le développement des implémentations du client et du service.

## <a name="where-applicable"></a>Le cas échéant

Les services Web sur les appareils permettent à un client de découvrir et d’accéder à un appareil distant et à ses services associés sur un réseau. Il prend en charge la découverte, la description, le contrôle et les événements des appareils. Les développeurs peuvent créer des proxys de client WSDAPI et les stubs correspondants pour les hôtes d’appareils.

## <a name="developer-audience"></a>Développeurs concernés

La documentation sur les appareils Web services sur les appareils est destinée aux programmeurs C/C++ et aux fournisseurs d’appareils qui créent des produits conformes à DPWS.

## <a name="run-time-requirements"></a>Conditions d’exécution

Les applications clientes qui utilisent WSDAPI sont prises en charge à partir de Windows Vista et de Windows Server 2008.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                  | Description                                                                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [À propos des services Web sur les appareils](about-web-services-for-devices.md)<br/>         | Informations architecturales et générales sur les services Web sur les appareils.<br/>              |
| [Utilisation de services Web sur des appareils](using-web-services-on-devices.md)<br/>          | Informations sur la génération de code, la configuration des applications et la résolution des problèmes.<br/> |
| [Informations de référence sur les services Web sur les appareils](web-services-for-devices-reference.md)<br/> | Documentation de référence sur l’API des services Web sur les appareils.<br/>                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Blog de Dan Driscoll](/archive/blogs/dandris/)
</dt> </dl>

 

