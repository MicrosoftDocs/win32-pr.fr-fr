---
title: Contrôle de l’utilisation du contenu
description: Contrôle de l’utilisation du contenu
ms.assetid: f87b5d95-a497-4356-817f-49ac3819df08
keywords:
- Windows Gestionnaire de périphériques de média, utilisation du contenu de contrôle
- Gestionnaire de périphériques, utilisation du contenu de contrôle
- Guide de programmation, utilisation du contenu de contrôle
- applications de bureau, utilisation du contenu de contrôle
- création d’applications de Gestionnaire de périphériques multimédia Windows, utilisation du contenu de contrôle
- contrôle de l’utilisation du contenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 649eee810e7bbdbc2ea93a32c6368ec345fa7364
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919464"
---
# <a name="metering-content-usage"></a>Contrôle de l’utilisation du contenu

avec la technologie Windows Media 10, vous pouvez désormais mesurer l’utilisation du contenu sur un appareil mobile. si une licence Windows Media 10 autorise le contrôle, l’appareil peut stocker le nombre de lecture des chansons et les télécharger à nouveau sur l’émetteur de licence via Internet. Ce système permet aux fournisseurs de contenu d’ajuster leurs frais de droits en mesurant précisément l’utilisation du contenu.

pour mesurer le contenu, l’application doit disposer d’un certificat de contrôle fourni par un service de gestion des licences basé sur le kit de développement logiciel (SDK) Windows Media Rights Manager 10. Seul le contenu concédé sous licence par ce même service peut être mesuré. pour plus d’informations sur le fonctionnement du contrôle et sur la création d’un service de contrôle de licence, consultez la [documentation Windows du kit de développement logiciel (SDK) Media Rights Manager](/previous-versions/ms986509(v=msdn.10)) sur MSDN. le kit de développement logiciel (SDK) peut être obtenu en remplissant les informations nécessaires sur la [Page Windows Media Licensing](https://www.microsoft.com/licensing/default).

une application peut avoir des mesures de contrôle intégrées, ou vous pouvez générer un plug-in COM pour une application existante, telle que la Lecteur Windows Media, si l’application accepte les plug-ins de contrôle.

Une application doit avertir les utilisateurs si l’utilisation du contenu est limitée. Pour plus d’informations, consultez les pages Web Microsoft listées dans la [déclaration de confidentialité](privacy-statement.md).

L’acquisition des données de contrôle à partir d’un appareil peut être lente. Par conséquent, si une application mesure son utilisation, elle doit le faire fréquemment pour empêcher l’accumulation de grandes quantités de données sur l’appareil et ralentir le transfert de données. Pour empêcher les transferts de données trop lents, les fabricants de périphériques peuvent envoyer des sous-ensembles de données de contrôle disponibles. L’application doit surveiller les indicateurs récupérés par [**IWMDRMDeviceApp ::P rocessmeterresponse**](iwmdrmdeviceapp-processmeterresponse.md) pour voir si d’autres données de contrôle sont conservées sur l’appareil.

Les étapes suivantes montrent comment une application peut mesurer l’utilisation du contenu.

1.  étant donné que le contrôle est uniquement disponible sur les appareils qui prennent en charge Windows Media DRM 10 pour les appareils mobiles, votre application doit à un moment donné appeler **QueryDeviceStatus**, comme décrit dans [gestion du contenu protégé dans l’application](handling-protected-content-in-the-application.md), pour garantir que l’appareil est valide et à jour.
2.  Demandez les informations de contrôle de l’appareil en appelant [**IWMDRMDeviceApp :: GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).
3.  Envoyez les données de contrôle récupérées au service de contrôle à l’URL récupérée par **GenerateMeterChallenge**. Le format des données envoyées au service dépend de l’écriture de scripts sur ce service particulier. Par exemple, certains services peuvent nécessiter que les données soient envoyées en tant que commande de publication sous la forme d’une paire nom/valeur. Le fournisseur de services doit vous permettre de connaître les exigences de mise en forme spécifiques.
4.  Obtenir une réponse du service de contrôle et l’envoyer à l’appareil en appelant [**IWMDRMDeviceApp ::P rocessmeterresponse**](iwmdrmdeviceapp-processmeterresponse.md). Cela amène l’appareil à réinitialiser les nombres de lecture et retourne également une valeur indiquant s’il existe des données de contrôle supplémentaires sur l’appareil qui doivent être récupérées en appelant à nouveau **GenerateMeterChallenge** .

pour obtenir des informations complètes et des exemples de code pour le contrôle, consultez le [site Web Windows Media](/previous-versions//bb614723(v=vs.85)).

 

 