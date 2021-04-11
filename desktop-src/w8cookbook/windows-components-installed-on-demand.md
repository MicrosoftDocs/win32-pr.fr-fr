---
title: Composants Windows installés à la demande
description: Composants Windows installés à la demande
ms.assetid: 14865DD7-167C-462C-B85A-BD07C929D7B8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d2c3c3fee1cd12d7b12900e41dc006badcf53f
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104031988"
---
# <a name="windows-components-installed-on-demand"></a>Composants Windows installés à la demande

## <a name="platform"></a>Plateforme

**Clients-** Windows 8.1  







## <a name="description"></a>Description

Deux composants Windows seront installés à la demande dans Windows 8.1 : DirectPlay et NTVDM. Ces composants sont répertoriés dans les composants facultatifs sous le nœud « composants hérités ». Ces composants sont installés localement dans le cadre du système d’exploitation et compressés en tant que composants facultatifs. Quand une application référence ou appelle l’un de ces composants (généralement au premier lancement de l’application), l’installation est déclenchée automatiquement. Les utilisateurs sont avertis que le composant sera installé et doivent confirmer l’action pour continuer. L’élévation est nécessaire pour que cette opération aboutisse si l’utilisateur n’est pas un administrateur. Après l’installation initiale, l’utilisateur n’a pas besoin d’effectuer d’autres actions pour réutiliser le composant.

## <a name="manifestation"></a>Manifestation

Quand une application référence ou appelle un composant hérité dans des composants facultatifs (au premier lancement), l’application est interrompue et la boîte de dialogue fonctionnalité à la demande s’ouvre et demande l’autorisation de l’utilisateur pour installer le composant. Si les utilisateurs cliquent sur OK, ils peuvent également voir une invite d’élévation dans laquelle ils doivent entrer leurs informations d’identification. Le composant sera alors installé et l’application reprendra.

## <a name="mitigation"></a>Limitation des risques

Pour que l’interface utilisateur des fonctionnalités à la demande ne s’ouvre pas, vous pouvez préinstaller DirectPlay et NTVDM à l’aide de DISM ou de l’interface utilisateur des composants facultatifs.

## <a name="solution"></a>Solution

Il est vivement recommandé d’éviter de référencer ou d’appeler des composants qui ont été répertoriés en tant que composants facultatifs hérités dans Windows dans les futures versions de votre application. Les composants facultatifs hérités incluent uniquement des composants plus anciens et moins utilisés qui pourraient provoquer des problèmes de performances et de sécurité pour les utilisateurs.

## <a name="tests"></a>Tests

Aucun aménagement de test supplémentaire n’est nécessaire pour la compatibilité. Il est important de savoir que cette boîte de dialogue apparaît lorsque le composant facultatif est appelé ou référencé, et que cette installation requiert une élévation.

 

 




