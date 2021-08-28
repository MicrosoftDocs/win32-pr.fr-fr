---
description: Inscription d’un DMO
ms.assetid: 9f74fc1c-b903-4725-b667-3c56a2726dbc
title: Inscription d’un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5635f7b05edb13da80adb62104db5c412fa55608ec2f9b5214380b7d9a095e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904539"
---
# <a name="registering-a-dmo"></a>Inscription d’un DMO

pour que les clients utilisent votre DMO, le CLSID doit être inscrit sur le système de l’utilisateur. Cette opération s’effectue par le biais de la fonction **DllRegisterServer** de la dll. Si vous utilisez la Active Template Library (ATL), l’Assistant ATL génère automatiquement cette fonction.

vous pouvez également inscrire votre DMO sous une ou plusieurs catégories de DMO standard. cela permet aux clients de découvrir votre DMO à l’aide de la fonction [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) . les catégories sont définies par le guid et sont répertoriées dans la section [DMO guid](dmo-guids.md).

l’inscription d’un DMO sous une catégorie est facultative. pour ce faire, appelez la fonction [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) et spécifiez le nom convivial de l’DMO, le CLSID et la catégorie. Si vous le souhaitez, vous pouvez également inscrire un ensemble de types de médias pris en charge par votre DMOs. pour plus d’informations, consultez [DMO Types de média](dmo-media-types.md).

l’exemple suivant montre comment enregistrer un effet audio DMO qui prend en charge l’entrée et la sortie audio PCM. Dans ce cas, les types d’entrée et de sortie sont les mêmes.


```C++
STDAPI DllRegisterServer(void)
{
    // Register the DMO as a PCM audio effect DMO
    DMO_PARTIAL_MEDIATYPE mt;
    mt.type    = MEDIATYPE_Audio;
    mt.subtype = MEDIASUBTYPE_PCM;
    HRESULT hr = DMORegister(
        L"MyDMO",                  // Friendly name
        CLSID_MyDMO,               // CLSID
        DMOCATEGORY_AUDIO_EFFECT,  // Category
        0,                         // Flags 
        1,                         // Number of input types
        &mt,                       // Array of input types
        1,                         // Number of output types
        &mt);                      // Array of output types

    if (FAILED(hr)) return hr;

    // Registers the object, with no typelib.
    return _Module.RegisterServer(FALSE);
}
```



Cet exemple suppose que ATL a été utilisé pour créer le projet. la dernière ligne de la fonction appelle la méthode ATL standard pour inscrire le serveur COM. Si vous n’utilisez pas ATL, votre fonction sera différente.

**Annulation de l’inscription d’un DMO**

Votre fonction **DllUnregisterServer** doit supprimer toutes les entrées de Registre créées par la fonction **DllRegisterServer** . si vous appelez **DMORegister** lorsque vous inscrivez le DMO, vous devez [**DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) avec la même catégorie quand vous annulez l’inscription de l’DMO.

L’exemple suivant supprime les entrées de Registre créées dans l’exemple précédent :


```C++
STDAPI DllUnregisterServer(void)
{
    DMOUnregister(CLSID_MyDMO, DMOCATEGORY_AUDIO_EFFECT);
    return _Module.UnregisterServer(TRUE);
}
```



**DirectShow Valeurs mérite**

dans le cadre de la création de graphiques de filtre, DirectShow affecte une valeur de mérite par défaut à DMOs. vous pouvez remplacer cette valeur en ajoutant une entrée de registre à la clé de registre de l’DMO dans HKEY \_ CLASSES \_ racine \\ CLSID. Incluez une valeur **DWORD** nommée `Merit` dont la valeur spécifie le mérite.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture d’un DMO](writing-a-dmo.md)
</dt> </dl>

 

 



