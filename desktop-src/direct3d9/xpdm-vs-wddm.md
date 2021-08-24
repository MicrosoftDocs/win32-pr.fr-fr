---
description: l’API Direct3D 9 fonctionne sur le modèle de pilote d’affichage (XPDM) Windows XP ou le modèle WDDM (Windows Vista display driver model), selon le système d’exploitation installé.
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: XPDM et WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0332198cd7c9425a3b5a107259dda1b1e974a04a2379244cdf939384260a89f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746049"
---
# <a name="xpdm-vs-wddm"></a>XPDM et WDDM

l’API Direct3D 9 fonctionne sur le modèle de pilote d’affichage (XPDM) Windows XP ou le modèle WDDM (Windows Vista display driver model), selon le système d’exploitation installé. Il existe des différences dans la façon dont l’API Direct3D se comporte sur les deux modèles de pilote.

-   [Bureau sécurisé](#secure-desktop)
-   [Bureau à distance](#remote-desktop)
-   [Service Windows](#windows-service)
-   [Rubriques connexes](#related-topics)

## <a name="secure-desktop"></a>Bureau sécurisé

le bureau sécurisé est actif lorsque l’un des éléments suivants se produit : l’utilisateur verrouille son bureau (Windows + L), l’économiseur d’écran s’active (quand aucun utilisateur n’est connecté) ou par défaut lorsque le contrôle de compte d’utilisateur affiche une invite. Lorsque le Bureau sécurisé est actif, le périphérique HAL n’est pas accessible.

Différences entre XPDM et WDDM :

- La tentative de création d’un appareil HAL Direct3D9 échoue (avec **D3DERR \_ non \_ disponible**) et tout périphérique Direct3D 9 existant indique qu’un code de retour de l’appareil a été perdu sur présent.

- Les API Direct3D9Ex et Direct3D 10 peuvent créer correctement un appareil alors que le Bureau sécurisé est actif et tous les appels à présent ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) ou dxgi) renvoient un code d’état indiquant que le bureau n’est pas disponible actuellement.



 

## <a name="remote-desktop"></a>Bureau à distance

Lorsqu’un bureau à distance est actif, l’affichage est géré par l’ordinateur d’affichage et l’ordinateur hôte envoie des informations via le réseau.

Différences entre XPDM et WDDM :

- Sur XPDM, toutes les tentatives de création d’un périphérique Direct3D 9 sur un bureau à distance échouent.

- Sur WDDM, le Bureau à distance prend en charge la création d’un appareil HAL via une session Bureau à distance.



 

## <a name="windows-service"></a>Service Windows

un service Windows est un processus qui s’exécute en arrière-plan, contrôlé par le gestionnaire de contrôle des services (SCM). Un service s’exécute indépendamment du bureau actif et dispose donc d’une capacité d’interaction limitée avec les utilisateurs.

Différences entre XPDM et WDDM :

- sur WDDM, l’Isolation de la Session 0 garantit qu’un service n’a pas accès aux postes de travail des utilisateurs comme mesure de sécurité. par conséquent, un appareil HAL de Direct3D 9 n’est jamais disponible à partir d’un service de Windows.



 

> [!Note]  
> vous ne pouvez pas utiliser Direct3D 9 dans un service de Windows. Pour plus d’informations, consultez [l’article du support technique Microsoft 978635](https://support.microsoft.com/kb/978635).

 


Le tableau suivant récapitule les différences répertoriées ici.



| Bureau sécurisé | XPDM | WDDM (Direct3D9) | WDDM (Direct3D9Ex/Direct3D10) |
|-----------------|------|------------------|------------------------------|
| NULLREF         | Oui  | Oui              | Oui                          |
| COUCHE             | Non   | Non               | Oui                          |
| REF             | Oui  | Oui              | Oui                          |
| Bureau à distance  |      |                  |                              |
| NULLREF         | Non   | Oui              | Oui                          |
| COUCHE             | Non   | Oui              | Oui                          |
| REF             | Oui  | Oui              | Oui                          |
| Service Windows |      |                  |                              |
| NULLREF         | Non   | Non               | Non                           |
| COUCHE             | Non   | Non               | Non                           |
| REF             | Non   | Non               | Non                           |
| WARP10          | N/A  | N/A              | Oui                          |



 

Pour plus d’informations sur XPDM, WDDM, Direct3D9Ex et Direct3D 10, consultez [API Graphics dans Windows](../direct3darticles/graphics-apis-in-windows-vista.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Périphériques Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
