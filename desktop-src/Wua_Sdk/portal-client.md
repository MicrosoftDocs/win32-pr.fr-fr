---
description: l’API Windows Update Agent (WUA) est un ensemble d’interfaces COM qui permettent aux administrateurs système et aux programmeurs d’accéder à Windows Update et Windows Server Update Services (WSUS).
ms.assetid: 611dc759-e0fc-472e-bdc2-fb952ba74999
title: Windows Mettre à jour l’API d’agent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82e7e2c79a707424128082f8f3123cb5fff506a9fc98203ab1fdf8063393310d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738001"
---
# <a name="windows-update-agent-api"></a>Windows Mettre à jour l’API d’agent

## <a name="purpose"></a>Objectif

l’API Windows Update Agent (WUA) est un ensemble d’interfaces COM qui permettent aux administrateurs système et aux programmeurs d’accéder à Windows Update et [Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85)). Les scripts et les programmes peuvent être écrits pour examiner les mises à jour actuellement disponibles pour un ordinateur, puis vous pouvez installer ou désinstaller des mises à jour.

## <a name="where-applicable"></a>Le cas échéant

Les administrateurs système peuvent utiliser WUA pour déterminer par programmation les mises à jour à appliquer à un ordinateur, télécharger ces mises à jour, puis les installer avec peu ou pas d’intervention de l’utilisateur.

Les éditeurs de logiciels indépendants (ISV) et les développeurs d’utilisateurs finaux peuvent intégrer les fonctionnalités de WUA dans le logiciel de gestion d’ordinateur ou de gestion des mises à jour pour fournir un environnement d’exploitation transparent.

## <a name="developer-audience"></a>Développeurs concernés

Vous pouvez écrire des applications WUA dans plusieurs langages de programmation. WUA définit des interfaces et des objets accessibles à partir de Visual Basic, Visual Basic scripting Edition (VBScript), JScript et à partir de C et C++. Une bonne connaissance de la programmation COM est utile pour le programmeur WUA.

## <a name="run-time-requirements"></a>Conditions d’exécution

WUA est pris en charge à partir de Windows XP. WUA est pris en charge sur le serveur à partir de Windows server 2003.

## <a name="in-this-section"></a>Dans cette section

-   [utilisation de l’API Windows Update Agent](using-the-windows-update-agent-api.md)
-   [Informations de référence sur l’API WUA](windows-update-agent--wua--api-reference.md)

 

 
