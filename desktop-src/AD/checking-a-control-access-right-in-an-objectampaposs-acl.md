---
title: Vérification d’un droit d’accès de contrôle dans la liste de contrôle d’accès d’un objet
description: Pour vérifier un droit d’accès au contrôle dans la liste de contrôle d’accès d’un objet, utilisez la fonction AccessCheckByTypeResultList.
ms.assetid: 5a609622-6a1a-46ae-a336-afec504225c7
ms.tgt_platform: multiple
keywords:
- Vérification d’un droit d’accès de contrôle dans une liste de contrôle d’accès d’objet Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10170bd496da14657356a2334015975da1cc02ff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031047"
---
# <a name="checking-a-control-access-right-in-an-objects-acl"></a>Vérification d’un droit d’accès de contrôle dans la liste de contrôle d’accès d’un objet

Pour vérifier un droit d’accès au contrôle dans la liste de contrôle d’accès d’un objet, utilisez la fonction [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) . Pour utiliser cette fonction, une application requiert un pointeur vers le [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) de l’objet au lieu d’une interface [**IADSSECURITYDESCRIPTOR**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) vers un objet com du descripteur de sécurité ADSI.

Procédez comme suit pour vérifier l’accès pour un droit d’accès contrôlé sur un objet :

1.  Obtient un pointeur d’interface [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) vers l’objet.
2.  Utilisez la méthode [**IDirectoryObject :: GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) pour récupérer le descripteur de sécurité de l’objet. Le nom de la propriété contenant le descripteur de sécurité est [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor). La propriété est retournée en tant que pointeur vers une structure de [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) .
3.  Utilisez la structure du [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) avec la fonction [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) pour vérifier les autorisations pour le droit d’accès du contrôle spécifié pour le client spécifié.

L’exemple de code dans l' [exemple de code pour la vérification d’un droit d’accès de contrôle dans l’ACL d’un objet](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) montre, en détail, comment procéder.

 

 