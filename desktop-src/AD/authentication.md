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
ms.openlocfilehash: 87eb07e05b9f817d894c13d089cf9ec1291ca14b58b640c9a4c26ae9cff8c44d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024220"
---
# <a name="authentication-ad-ds"></a>Authentification (AD DS)

Chaque objet dans Active Directory Domain Services possède un descripteur de sécurité unique qui définit les autorisations d’accès requises pour lire ou mettre à jour l’objet ou ses propriétés individuelles. Les privilèges d’accès sont déterminés par les droits accordés au compte d’un utilisateur ou aux appartenances à un groupe.

Quand une application est liée à un objet dans l’annuaire, les privilèges d’accès de l’application à cet objet sont basés sur le contexte utilisateur spécifié pendant l’opération de liaison. Pour les fonctions de liaison et les méthodes [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject), [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject), **GetObject**, [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject), une application peut utiliser implicitement les informations d’identification de l’appelant, spécifier explicitement les informations d’identification d’un compte d’utilisateur ou utiliser un contexte utilisateur non authentifié (invité).

 

 