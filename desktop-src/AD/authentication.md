---
title: Authentification (AD DS)
description: Chaque objet dans Active Directory Domain Services possède un descripteur de sécurité unique qui définit les autorisations d’accès requises pour lire ou mettre à jour l’objet ou ses propriétés individuelles.
ms.assetid: a4a663d3-b0f3-4993-a74e-9e4f896e8c95
ms.tgt_platform: multiple
keywords:
- Active Directory, utilisation de, liaison, authentification
- liaison de l’authentification Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb80bbca4604a99011d3198eaf6b3e871cd3f84c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462935"
---
# <a name="authentication-ad-ds"></a>Authentification (AD DS)

Chaque objet dans Active Directory Domain Services possède un descripteur de sécurité unique qui définit les autorisations d’accès requises pour lire ou mettre à jour l’objet ou ses propriétés individuelles. Les privilèges d’accès sont déterminés par les droits accordés au compte d’un utilisateur ou aux appartenances à un groupe.

Quand une application est liée à un objet dans l’annuaire, les privilèges d’accès de l’application à cet objet sont basés sur le contexte utilisateur spécifié pendant l’opération de liaison. Pour les fonctions de liaison et les méthodes [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject), [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject), **GetObject**, [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject), une application peut utiliser implicitement les informations d’identification de l’appelant, spécifier explicitement les informations d’identification d’un compte d’utilisateur ou utiliser un contexte utilisateur non authentifié (invité).

 

 