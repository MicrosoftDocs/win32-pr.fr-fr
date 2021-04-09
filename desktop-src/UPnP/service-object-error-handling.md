---
title: Gestion des erreurs des objets de service
description: Lorsqu’une erreur se produit dans un objet de service, la valeur de retour de l’appel IDispatch Invoke doit être DISP \_ E \_ exception, et le pointeur de paramètre pExceptInfo vers une structure EXCEPTINFO dans le doit être renseigné.
ms.assetid: 1b08c404-69f2-4b0d-9231-c2bd242e124d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fd39d08dc7ca5152ca412df1a6fb67d6df524f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101800"
---
# <a name="service-object-error-handling"></a>Gestion des erreurs des objets de service

Lorsqu’une erreur se produit dans un objet de service, la valeur de retour de l’appel [**IDispatch :: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) doit être DISP \_ E \_ exception, et le pointeur de paramètre *pExceptInfo* vers une structure [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) dans le doit être renseigné.

Plus précisément, les membres **bstrSource** et **bstrDescription** de la structure [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) sont utilisés par l’hôte d’appareil avec la technologie UPnP pour créer une réponse d’erreur UPnP. **bstrSource** est le code d’erreur et **bstrDescription** est la description de l’erreur.

 

 