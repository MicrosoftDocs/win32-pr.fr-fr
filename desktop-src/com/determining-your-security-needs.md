---
title: Détermination de vos besoins en matière de sécurité
description: La façon dont vous configurez la sécurité COM pour votre application dépend du type de sécurité dont votre application a besoin. Il existe plusieurs situations courantes qui déterminent ce que vous devez faire.
ms.assetid: db5c9adb-b04b-4621-b738-2959cac40985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cacef6d4e3aab59cb3b603125c36dd17d07846
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675822"
---
# <a name="determining-your-security-needs"></a>Détermination de vos besoins en matière de sécurité

La façon dont vous configurez la sécurité COM pour votre application dépend du type de sécurité dont votre application a besoin. Il existe plusieurs situations courantes qui déterminent ce que vous devez faire.

Si vous décidez d’utiliser les valeurs par défaut de sécurité COM, vous n’avez pas à faire anythingâ. COM les gère tous. Pour plus d’informations sur ce que sont ces paramètres par défaut, consultez [valeurs par défaut de la sécurité com](com-security-defaults.md).

Vous pouvez également empêcher tout appel distant sur votre ordinateur en désactivant DCOM (COM entre les ordinateurs distants). Pour plus d’informations, consultez Définition de la [sécurité System-Wide à l’aide de DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).

Pour les applications héritées ou nouvelles, vous pouvez définir la sécurité au niveau du processus dans le registre. Pour plus d’informations, consultez [définition de la sécurité échelle dans le registre](setting-processwide-security-through-the-registry.md).

Vous pouvez également remplacer les paramètres de sécurité par défaut pour les appels à certaines interfaces dans le processus lors de la définition de la sécurité par défaut pour le reste du processus (pour permettre à COM de gérer les cas généraux). Pour plus d’informations, consultez [définition de la sécurité au niveau du proxy de l’interface](setting-security-at-the-interface-proxy-level.md).

Pour les exigences de sécurité complexes, vous pouvez gérer l’ensemble de la sécurité par programmation plutôt que de permettre à COM de la gérer à votre place. Pour ce faire, appelez [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) pour désactiver l’authentification automatique, puis Contrôlez tous les paramètres de sécurité en définissant la sécurité sur une base de proxy par interface. Pour plus d’informations, consultez Définition de la [sécurité échelle avec CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md) et [définition de la sécurité au niveau du proxy d’interface](setting-security-at-the-interface-proxy-level.md).

Dans certains scénarios, vous souhaiterez peut-être désactiver complètement la sécurité. Vous pouvez décider que votre application n’a pas besoin de sécurité, ou vous souhaiterez peut-être désactiver la sécurité pendant le développement afin que vous puissiez activer les fonctionnalités de sécurité individuellement. Pour savoir comment désactiver la sécurité COM, consultez Désactivation de la [sécurité](turning-off-security.md).

La sécurité dans COM s’appuie sur les services d’authentification administrés par les packages de sécurité. NTLMSSP fonctionne bien pour de nombreuses applications, mais il ne fournit pas la sécurité la plus robuste offerte par d’autres packages. Par conséquent, COM prend en charge le package de sécurité Schannel et le protocole de sécurité Kerberos V5. Pour plus d’informations sur l’utilisation de ces packages de sécurité, consultez [com et packages de sécurité](com-and-security-packages.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sécurité dans COM](security-in-com.md)
</dt> </dl>

 

 




