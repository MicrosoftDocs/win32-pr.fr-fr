---
description: à partir de Windows 8, l' \_ infrastructure des dll AppInit est désactivée lorsque le démarrage sécurisé est activé.
ms.assetid: 3ADE71C7-7113-4D26-8D6D-5609CAF13397
title: DLL AppInit et démarrage sécurisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67db758eebbccd1916b5c2611c20598c3f4d25cc80cd2910be22a65b4222bbae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119256019"
---
# <a name="appinit-dlls-and-secure-boot"></a>DLL AppInit et démarrage sécurisé

à partir de Windows 8, l' \_ infrastructure des dll AppInit est désactivée lorsque le démarrage sécurisé est activé.

## <a name="about-appinit_dlls"></a>À propos des \_ DLL AppInit

L' \_ infrastructure des DLL AppInit offre un moyen simple de raccorder les API système en autorisant le chargement des dll personnalisées dans l’espace d’adressage de chaque application interactive. Les applications et les programmes malveillants utilisent tous deux des DLL AppInit pour la même raison de base, qui consiste à raccorder des API. une fois la DLL personnalisée chargée, elle peut raccorder une API système connue et implémenter d’autres fonctionnalités. Seul un petit ensemble d’applications légitimes modernes utilise ce mécanisme pour charger les dll, tandis qu’un grand ensemble de programmes malveillants utilisent ce mécanisme pour compromettre les systèmes. Même les DLL AppInit légitimes \_ peuvent provoquer des blocages système et des problèmes de performances, par conséquent, l’utilisation de \_ DLL AppInit n’est pas recommandée.

## <a name="appinit_dlls-and-secure-boot"></a>\_DLL appInit et démarrage sécurisé

Windows 8 a adopté UEFI et le démarrage sécurisé pour améliorer l’intégrité globale du système et fournir une protection renforcée contre les menaces sophistiquées. Lorsque le démarrage sécurisé est activé, le \_ mécanisme des DLL AppInit est désactivé dans le cadre d’une approche sans compromis pour protéger les clients contre les logiciels malveillants et les menaces.

notez que le démarrage sécurisé est un protocole UEFI et non une fonctionnalité de Windows 8. Pour plus d’informations sur UEFI et sur la spécification du protocole de démarrage sécurisé, consultez [https://www.uefi.org](https://www.uefi.org/) .

## <a name="appinit_dlls-certification-requirement-for-windows-8-desktop-apps"></a>\_conditions de certification des dll AppInit pour les applications de bureau Windows 8

l’une des conditions de certification pour les applications de bureau Windows 8 est que l’application ne doit pas charger de dll arbitraires pour intercepter les appels d’API Win32 à l’aide du \_ mécanisme de dll AppInit. pour plus d’informations sur les conditions requises en matière de certification, reportez-vous à la section 1,1 des [conditions de certification pour Windows 8 les applications de bureau](../win_cert/certification-requirements-for-windows-desktop-apps.md).

## <a name="summary"></a>Récapitulatif

-   Le \_ mécanisme des DLL AppInit n’est pas une approche recommandée pour les applications légitimes, car cela peut entraîner des blocages système et des problèmes de performances.
-   Le \_ mécanisme des DLL AppInit est désactivé par défaut lorsque le démarrage sécurisé est activé.
-   l’utilisation \_ de dll AppInit dans une application de bureau Windows 8 est une Windows échec de la certification des applications de bureau.

consultez le livre blanc suivant pour plus d’informations sur les \_ dll AppInit sur Windows 7 et Windows server 2008 r2 : [dll AppInit dans Windows 7 et Windows server 2008 R2](/previous-versions/windows/hardware/download/dn550976(v=vs.85)).

 

 
