---
title: Sauvegarde et restauration de licences DRM
description: Sauvegarde et restauration de licences DRM
ms.assetid: ec2777e9-76af-43fe-8bd5-4d7532d2fb32
keywords:
- Windows Media Format SDK, sauvegarde des licences DRM
- Windows Media Format SDK, restauration de licences DRM
- Windows Kit de développement logiciel (SDK) Media format, licences DRM
- Windows Media Format SDK, licences pour DRM
- Windows Media Format SDK, fonctionnalité de restauration de sauvegarde
- Windows Media Format SDK, service de gestion des licences
- Windows Media Format SDK, détection des fraudes
- gestion des droits numériques (DRM), sauvegarde des licences
- DRM (gestion des droits numériques), sauvegarde des licences
- gestion des droits numériques (DRM), restauration des licences
- DRM (gestion des droits numériques), restauration des licences
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- gestion des droits numériques (DRM), fonctionnalité de restauration de sauvegarde
- DRM (gestion des droits numériques), fonctionnalité de restauration de sauvegarde
- gestion des droits numériques (DRM), service de gestion de licences
- DRM (gestion des droits numériques), service de gestion des licences
- gestion des droits numériques (DRM), détection des fraudes
- DRM (gestion des droits numériques), détection des fraudes
- sauvegarde des licences DRM
- restauration des licences DRM
- licences, DRM
- licences, sauvegarde de DRM
- licences, restauration de DRM
- Fonctionnalité de restauration de sauvegarde
- Service de gestion des licences
- détection des fraudes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 019163a42312b14b7d7b7e15cea68be1996a976e42b31491f62486a43d37b8bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028147"
---
# <a name="backing-up-and-restoring-of-drm-licenses"></a>Sauvegarde et restauration de licences DRM

Avec la fonction de restauration de sauvegarde, les utilisateurs peuvent sauvegarder et restaurer des [*licences*](wmformat-glossary.md) sur le même ordinateur ou sur d’autres ordinateurs. Cette fonctionnalité permet aux utilisateurs de transférer des licences vers un nouvel ordinateur ou de les replacer sur le même ordinateur (après avoir reformatage du disque dur, par exemple). En outre, les utilisateurs peuvent lire des fichiers ASF protégés sur plusieurs ordinateurs.

Pour encourager l’utilisation légitime d’une licence, une stratégie de détection des fraudes restreint le nombre de fois qu’une licence peut être restaurée. Microsoft fournit un service qui effectue le suivi du nombre d’ordinateurs sur lesquels une licence a été restaurée. Si une limite est atteinte, l’utilisateur ne peut pas restaurer la licence.

## <a name="allowing-or-disallowing-the-right-to-back-up-and-restore"></a>Autoriser ou non le droit de sauvegarder et de restaurer

La fonction de restauration de sauvegarde fonctionne uniquement pour les licences pour lesquelles le droit de sauvegarde et de restauration est donné. Si les propriétaires de contenu ou les émetteurs de licence ne souhaitent pas cette fonctionnalité, ou s’ils émettent des licences qui contiennent un état sécurisé (par exemple, des opérations comptées ou une durée limitée), ils peuvent interdire ce droit.

Quand une licence ne peut pas être restaurée parce qu’un utilisateur n’a pas le droit, un [*ID de clé*](wmformat-glossary.md) est passé à l’application. Au minimum, l’utilisateur doit être informé que certaines licences n’ont pas pu être sauvegardées, même si l’utilisateur ne connaît pas les licences auxquelles ce message fait référence. Si vous connaissez l’ID de clé pour les fichiers protégés disponibles, vous pouvez développer une solution plus robuste pour informer l’utilisateur.

Par exemple, un joueur peut être développé pour une étiquette d’enregistrement qui fournit des chansons protégées sur Internet. Ces chansons et leurs ID de clé peuvent être suivis dans une base de données. Si certaines licences n’ont pas pu être sauvegardées, l’application de lecteur peut utiliser l’ID de clé pour interroger la base de données afin d’obtenir le nom des chansons, puis informer l’utilisateur des chansons pour lesquelles les licences ne peuvent pas être sauvegardées. Ou bien, une bibliothèque musicale peut être créée pour chaque utilisateur localement, et l’ID de clé peut être utilisé pour récupérer des informations supplémentaires sur les licences qui n’ont pas pu être sauvegardées.

## <a name="the-license-management-service"></a>Service de gestion des licences

Lorsque la fonctionnalité de restauration de la sauvegarde est implémentée, un service de gestion des licences hébergé par Microsoft gère la restauration des licences.

Tout d’abord, les utilisateurs sauvegardent les licences dans l’application, par exemple, en choisissant une option de menu. Toutes les licences sur l’ordinateur sont sauvegardées à un emplacement spécifié, par exemple une disquette. Ensuite, les utilisateurs restaurent les licences à l’aide de l’application, par exemple, en choisissant une option de menu et en spécifiant leur emplacement de sauvegarde.

À ce stade, l’utilisateur doit être connecté à Internet ; une demande de l’application est envoyée au service de gestion des licences. Si l’ordinateur à partir duquel la licence a été sauvegardée est différent de l’ordinateur d’origine (ou si l’ordinateur d’origine a été reformaté), le service de gestion des licences émet une nouvelle licence sur le nouvel ordinateur. Dans le cas contraire, la licence précédemment émise pour cet ordinateur est réémise.

Étant donné que le service de gestion des licences récupère les informations de l’utilisateur, vous devez afficher la politique de confidentialité de Microsoft ou fournir un lien vers cette page sur le [site Web de Microsoft](https://www.microsoft.com/licensing/default).

> [!Note]  
> Lorsqu’un utilisateur final restaure une licence sur un autre ordinateur et que la licence requiert une individualisation, l’utilisateur final doit autoriser les composants DRM à être mis à jour. Vous devez implémenter un processus dans votre application de lecteur pour prendre en charge cette fonctionnalité.

 

## <a name="detecting-fraud"></a>Détection des fraudes

L’utilisateur est autorisé à restaurer une licence un nombre limité de fois. Chaque fois qu’une licence est restaurée, le service de gestion des licences la suit et incrémente le nombre de cette licence d’une unité. Lors de la restauration d’une licence sur un ordinateur sur lequel la licence a été restaurée précédemment (par exemple, l’ordinateur à partir duquel la licence a été sauvegardée), le nombre n’est pas augmenté. Un ordinateur est considéré comme différent s’il dispose d’un nouveau système d’exploitation ou si le système d’exploitation a été réinstallé.

Conformément à la stratégie de détection des fraudes de Microsoft, lorsqu’une licence a été restaurée un certain nombre de fois, l’application reçoit une URL à partir des composants DRM et est chargée d’ouvrir un navigateur et d’afficher la page Web, ce qui indique que le contrat de licence n’a peut-être pas été respecté. L’utilisateur doit contacter le distributeur de licences, qui doit ensuite déterminer si la demande est valide.

> [!Note]  
> DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités de Rights Management numérique**](digital-rights-management-features.md)
</dt> <dt>

[**Sauvegarde et restauration de licences**](backing-up-and-restoring-licenses.md)
</dt> </dl>

 

 




