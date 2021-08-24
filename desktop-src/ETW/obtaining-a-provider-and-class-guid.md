---
description: Pour obtenir un GUID de fournisseur ou des GUID de classe de trace d’événements, vous pouvez utiliser l’outil Uuidgen.exe ou Guidgen.exe.
ms.assetid: 07483a78-ee67-4586-a75b-d376aa3351b7
title: Obtention d’un GUID de fournisseur et de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c480a45a5a826d3f258ab267e39db87bc85fad799fef5d7397a7c900f4872f22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914349"
---
# <a name="obtaining-a-provider-and-class-guid"></a>Obtention d’un GUID de fournisseur et de classe

Pour obtenir un GUID de fournisseur ou des GUID de classe de trace d’événements, vous pouvez utiliser l’outil Uuidgen.exe ou Guidgen.exe.

Si vous utilisez l’outil Uuidgen.exe, utilisez l’option-d pour créer une macro définir le \_ GUID C, comme indiqué dans l’exemple suivant. Pour plus d’informations sur l’utilisation de l’outil Uuidgen.exe, utilisez l’outil- ? option. Si vous utilisez la macro définir le \_ GUID C pour définir votre GUID, vous devez inclure \# define INITGUID avant vos définitions GUID, comme indiqué dans l’exemple suivant.

``` syntax
#define INITGUID

DEFINE_GUID (
  ProviderGuid,
  0xf4dc272d, 
  0x88dd, 
  0x4472, 
  0xa3, 0xb1, 0xcb, 0x6d, 0xa4, 0x86, 0xf0, 0xbe
  );
```

le kit de développement logiciel (SDK) de Microsoft Windows et Microsoft Visual Studio incluent l’outil Guidgen.exe. L’outil Guidgen.exe dispose d’une interface utilisateur qui vous permet de sélectionner différents formats. Vous devez utiliser le format qui crée un GUID de constante statique, comme indiqué dans l’exemple suivant.

``` syntax
// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };
```

 

 



