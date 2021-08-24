---
title: Licences
description: Licences
ms.assetid: a77c0141-62b4-4032-a734-5a55da6a50e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3058bd6bb543f2f3fc97f2e6a851b456638128c6e731050237aa0d36b12d681
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567739"
---
# <a name="licensing"></a>Licences

afin d’incorporer correctement les contrôles sous licence, ActiveX conteneurs de contrôle doivent utiliser [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) au lieu de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). plusieurs fonctions d’assistance pour la création et le chargement OLE ([**OleLoad**](/windows/desktop/api/Ole2/nf-ole2-oleload) et [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) appellent explicitement **IClassFactory** et not **IClassFactory2**, et ne peuvent donc pas être utilisées pour créer ou charger des contrôles de ActiveX sous licence. ActiveX conteneurs de contrôle doivent créer et charger explicitement des contrôles ActiveX à l’aide de **IClassFactory2**.

 

 