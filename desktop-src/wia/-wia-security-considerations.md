---
description: Ce document fournit des informations sur les considérations de sécurité liées à l’acquisition d’images Windows (WIA).
ms.assetid: 35455320-7d08-49de-938d-40dc0873917b
title: 'Considérations relatives à la sécurité : acquisition d’images Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ab080582492a0c03eab7879624bfb49a370e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514627"
---
# <a name="security-considerations-windows-image-acquisition"></a>Considérations relatives à la sécurité : acquisition d’images Windows

Ce document fournit des informations sur les considérations de sécurité liées à l’acquisition d’images Windows (WIA). Ce document ne fournit pas tout ce que vous devez savoir sur les problèmes de sécurité. Utilisez-le plutôt comme point de départ et référence pour ce domaine technologique.

-   [Utiliser des guillemets autour des noms de chemins](#use-quotation-marks-around-path-names)
-   [Placer les applications inscrites dans des emplacements sécurisés](#place-registered-applications-in-secure-locations)
-   [N’utilisez pas les répertoires ou les clés de Registre sous-jacents](#do-not-use-underlying-directories-or-registry-keys)
-   [Rubriques connexes](#related-topics)

## <a name="use-quotation-marks-around-path-names"></a>Utiliser des guillemets autour des noms de chemins

Quand vous utilisez [**IWiaDevMgr :: RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) pour inscrire une application pour recevoir des événements de périphérique, veillez à placer le chemin d’accès et le nom de fichier de l’application entre guillemets. Cela évite de faire en sorte que le chemin d’accès soit mal interprété et qu’une application non autorisée soit exécutée.

## <a name="place-registered-applications-in-secure-locations"></a>Placer les applications inscrites dans des emplacements sécurisés

Lorsqu’une application est inscrite pour recevoir un événement d’appareil, cette application peut être exécutée par n’importe quel utilisateur ayant accès à cet appareil. Par exemple, si une application est inscrite pour un événement d’analyse, le fait d’appuyer sur le bouton « Scan » (analyser) sur un scanneur entraîne l’exécution de cette application. Si l’application s’exécute avec un privilège plus élevé que celui de l’utilisateur, cela provoque un problème de sécurité potentiel.

## <a name="do-not-use-underlying-directories-or-registry-keys"></a>N’utilisez pas les répertoires ou les clés de Registre sous-jacents

WIA utilise plusieurs répertoires et clés de registre en interne pour stocker des données ou des informations. N’accédez pas directement à ces répertoires ou clés de registre. Utilisez plutôt les méthodes d’interface exposées pour spécifier des répertoires pour les images acquises.

## <a name="related-topics"></a>Rubriques connexes

-   [Sécurité Microsoft](https://www.microsoft.com/security/)
-   [Page d’hébergement sur la sécurité de MSDN Library](https://msdn.microsoft.com/security/default.aspx)
-   [Ressources de procédures pour la sécurité](https://www.microsoft.com/technet/solutionaccelerators/howto/sechow.mspx)
-   [Ressources de sécurité TechNet](https://technet.microsoft.com/security/default.aspx)
-   [Considérations sur la sécurité pour les développeurs Windows XP Embedded](/previous-versions/ms838345(v=msdn.10))
-   [Meilleures pratiques de sécurité](../secbp/best-practices-for-the-security-apis.md)

 

 
