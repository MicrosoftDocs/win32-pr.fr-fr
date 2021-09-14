---
title: Licences
description: Licences
ms.assetid: a77c0141-62b4-4032-a734-5a55da6a50e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06066365d2cf00a7b5db6d6ca755261e5a9470fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127216633"
---
# <a name="licensing"></a>Licences

afin d’incorporer correctement les contrôles sous licence, ActiveX conteneurs de contrôle doivent utiliser [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) au lieu de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). plusieurs fonctions d’assistance pour la création et le chargement OLE ([**OleLoad**](/windows/desktop/api/Ole2/nf-ole2-oleload) et [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) appellent explicitement **IClassFactory** et not **IClassFactory2**, et ne peuvent donc pas être utilisées pour créer ou charger des contrôles de ActiveX sous licence. ActiveX conteneurs de contrôle doivent créer et charger explicitement des contrôles ActiveX à l’aide de **IClassFactory2**.

 

 