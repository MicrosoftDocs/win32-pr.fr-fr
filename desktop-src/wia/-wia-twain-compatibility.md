---
description: WIA fournit une couche de compatibilité TWAIN qui permet aux applications compatibles TWAIN de communiquer avec les périphériques WIA (Windows Image Acquisition).
ms.assetid: 8e5673b9-c234-4722-b244-41aae015ac0c
title: Compatibilité avec TWAIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afc7d0beb9a6001a0cbb4dc0bc032cf4df781736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516675"
---
# <a name="twain-compatibility"></a>Compatibilité avec TWAIN

WIA fournit une couche de compatibilité TWAIN qui permet aux applications compatibles TWAIN de communiquer avec les périphériques WIA (Windows Image Acquisition). Les applications compatibles TWAIN n’ont pas un accès complet à la fonctionnalité WIA. Par exemple, une application ne peut pas supprimer l’interface utilisateur à l’aide de la couche de compatibilité TWAIN.

Les périphériques WIA apparaissent deux fois pour une application qui est consciente de WIA et TWAIN : une fois par le biais d’une communication WIA normale et une fois par le biais de la couche de compatibilité TWAIN. Pour éviter de répertorier deux fois un appareil WIA, une application qui prend en charge WIA et TWAIN doit filtrer les appareils WIA qui passent par la couche de compatibilité TWAIN. Tous les appareils WIA qui passent par la couche de compatibilité TWAIN ont un préfixe « WIA ». il est donc facile de les filtrer.

 

 



