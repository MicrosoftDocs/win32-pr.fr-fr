---
description: WIA fournit une couche de compatibilité twain qui permet aux applications compatibles twain de communiquer avec les appareils Windows d’Acquisition d’images (WIA).
ms.assetid: 8e5673b9-c234-4722-b244-41aae015ac0c
title: Compatibilité avec TWAIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3633dfc97a5356f2d63dd2d377e798312a9a2fb10fd03144222e5ed3b4fd0dc2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056979"
---
# <a name="twain-compatibility"></a>Compatibilité avec TWAIN

WIA fournit une couche de compatibilité twain qui permet aux applications compatibles twain de communiquer avec les appareils Windows d’Acquisition d’images (WIA). Les applications compatibles TWAIN n’ont pas un accès complet à la fonctionnalité WIA. Par exemple, une application ne peut pas supprimer l’interface utilisateur à l’aide de la couche de compatibilité TWAIN.

Les périphériques WIA apparaissent deux fois pour une application qui est consciente de WIA et TWAIN : une fois par le biais d’une communication WIA normale et une fois par le biais de la couche de compatibilité TWAIN. Pour éviter de répertorier deux fois un appareil WIA, une application qui prend en charge WIA et TWAIN doit filtrer les appareils WIA qui passent par la couche de compatibilité TWAIN. Tous les appareils WIA qui passent par la couche de compatibilité TWAIN ont un préfixe « WIA ». il est donc facile de les filtrer.

 

 



