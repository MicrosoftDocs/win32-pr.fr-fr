---
title: Gestion des erreurs des objets de service
description: Lorsqu’une erreur se produit dans un objet de service, la valeur de retour de l’appel IDispatch Invoke doit être DISP \_ E \_ exception, et le pointeur de paramètre pExceptInfo vers une structure EXCEPTINFO dans le doit être renseigné.
ms.assetid: 1b08c404-69f2-4b0d-9231-c2bd242e124d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c98db4ffdb3c4625ec4c0dfbe3d497ab1cbe4b5152b172c34422c1630ce581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999519"
---
# <a name="service-object-error-handling"></a>Gestion des erreurs des objets de service

Lorsqu’une erreur se produit dans un objet de service, la valeur de retour de l’appel [**IDispatch :: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) doit être DISP \_ E \_ exception, et le pointeur de paramètre *pExceptInfo* vers une structure [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) dans le doit être renseigné.

Plus précisément, les membres **bstrSource** et **bstrDescription** de la structure [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) sont utilisés par l’hôte d’appareil avec la technologie UPnP pour créer une réponse d’erreur UPnP. **bstrSource** est le code d’erreur et **bstrDescription** est la description de l’erreur.

 

 