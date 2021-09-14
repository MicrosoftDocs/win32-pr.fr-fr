---
description: Utilisé pour exécuter des tâches de façon asynchrone et créé avec D3DX10CreateThreadPump.
ms.assetid: 8d03c94a-9b64-464c-b0f4-4e5f5a00503f
title: Interface ID3DX10ThreadPump (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: aecab39b655998533c80f1fff56e3f10d941f551
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292058"
---
# <a name="id3dx10threadpump-interface"></a>Interface ID3DX10ThreadPump

Utilisé pour exécuter des tâches de façon asynchrone et créé avec [**D3DX10CreateThreadPump**](d3dx10createthreadpump.md). Plusieurs API D3DX10 peuvent éventuellement prendre une pompe de thread en tant que paramètre, comme [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) et [**D3DX10CompileFromFile**](d3dx10compilefromfile.md) (consultez la section Notes pour obtenir la liste complète). Si la pompe de threads est transmise à ces API, elles s’exécutent de façon asynchrone sur un thread de pompage de thread distinct. L’avantage de cette opération est qu’elle peut faire en sorte que le chargement et le traitement de grandes quantités de données se produisent sans voir un ralentissement des performances à l’écran.

## <a name="members"></a>Membres

L’interface **ID3DX10ThreadPump** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10ThreadPump** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX10ThreadPump** possède ces méthodes.



| Méthode                                                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddWorkItem**](id3dx10threadpump-addworkitem.md)                       | Ajoutez un élément de travail à la pompe de thread.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**GetQueueStatus**](id3dx10threadpump-getqueuestatus.md)                 | Obtient le nombre d’éléments dans chacune des trois files d’attente à l’intérieur de la pompe de thread.<br/>                                                                                                                                                                                                                                                                                                                                           |
| [**GetWorkItemCount**](id3dx10threadpump-getworkitemcount.md)             | Obtient le nombre d’éléments de travail actuellement dans la pompe de thread.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| [**ProcessDeviceWorkItems**](id3dx10threadpump-processdeviceworkitems.md) | Définissez les éléments de travail sur l’appareil une fois qu’ils ont terminé le chargement et le traitement. Lorsque la pompe de thread a terminé le chargement et le traitement d’une ressource ou d’un nuanceur, elle le contiendra dans une file d’attente jusqu’à ce que cette API soit appelée, auquel cas les éléments traités seront définis sur l’appareil. Cela est utile pour contrôler la quantité de traitement consacrée à la liaison de ressources à l’appareil pour chaque trame. Consultez la section Remarques.<br/> |
| [**PurgeAllItems**](id3dx10threadpump-purgeallitems.md)                   | Effacez tous les éléments de travail de la pompe de thread.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**WaitForAllItems**](id3dx10threadpump-waitforallitems.md)               | Attendez la fin de l’exécution de tous les éléments de travail de la pompe de thread.<br/>                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Notes

La pompe de thread charge et traite les données dans un processus en 3 étapes. Il va :

1.  Chargez et décompressez les données avec un chargeur de données. L’objet chargeur de données a trois méthodes que la pompe de thread appellera en interne lors du chargement et de la décompression des données : [**ID3DX10DataLoader :: Load**](id3dx10dataloader-load.md), [**ID3DX10DataLoader ::D eComPress**](id3dx10dataloader-decompress.md)et [**ID3DX10DataLoader ::D estroy**](id3dx10dataloader-destroy.md). La fonctionnalité spécifique de ces trois API diffère selon le type de données chargées et décompressées. L’interface de chargeur de données peut également être héritée et ses API peuvent être modifiées si l’une d’elles est en cours de chargement d’un fichier de données défini dans son propre format personnalisé.
2.  Traitez les données avec un processeur de données. L’objet de traitement de données a trois méthodes que la pompe de thread appellera en interne lors du traitement des données : [**ID3DX10DataProcessor ::P tionnaire**](id3dx10dataprocessor-process.md), [**ID3DX10DataProcessor :: CreateDeviceObject**](id3dx10dataprocessor-createdeviceobject.md)et [**ID3DX10DataProcessor ::D estroy**](id3dx10dataprocessor-destroy.md). La façon dont il traite les données est différente selon le type de données. Par exemple, si les données sont une texture stockée en tant que JPEG, **ID3DX10DataProcessor ::P tionnaire** effectue la décompression JPEG pour obtenir les bits d’image RAW de l’image. Si les données sont un nuanceur, **ID3DX10DataProcessor ::P tionnaire** compile le langage HLSL en bytecode. Une fois les données traitées, un objet périphérique sera créé pour ces données (avec **ID3DX10DataProcessor :: CreateDeviceObject**) et l’objet sera ajouté à une file d’attente d’objets périphériques. L’interface du processeur de données peut également être héritée et ses API peuvent être modifiées si l’une d’elles est en cours de traitement d’un fichier de données défini dans son propre format personnalisé.
3.  Liez l’objet appareil à l’appareil. Cette opération est effectuée quand une application appelle [**ID3DX10ThreadPump ::P rocessdeviceworkitems**](id3dx10threadpump-processdeviceworkitems.md), qui lie un nombre spécifié d’objets dans la file d’attente d’objets d’appareil à l’appareil.

La pompe de threads peut être utilisée pour charger des données de deux manières : en appelant une API qui prend une pompe de thread comme paramètre, tel que [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) et [**D3DX10CompileFromFile**](d3dx10compilefromfile.md), ou en appelant [**ID3DX10ThreadPump :: AddWorkItem**](id3dx10threadpump-addworkitem.md). Dans le cas des API qui prennent une pompe de thread, le chargeur de données et le processeur de données sont créés en interne. Dans le cas de **AddWorkItem**, le chargeur de données et le processeur de données doivent être créés au préalable et sont ensuite passés à AddWorkItem. D3DX10 fournit un ensemble d’API permettant de créer des chargeurs de données et des processeurs de données qui ont des fonctionnalités de chargement et de traitement des formats de données courants (consultez la section Notes pour obtenir la liste complète des API). Pour les formats de données personnalisés, les interfaces du chargeur de données et du processeur de données doivent être héritées et leurs méthodes doivent être redéfinies.

L’objet thread Pump occupe une quantité importante de ressources. en général, un seul doit être créé par application.

Chargeurs de données D3DX10 intégrés



|                                                                           |  Description                                        |
|----------------------------------------------------------------------------|------------------------------------------|
| [**D3DX10CreateAsyncFileLoader**](d3dx10createasyncfileloader.md)         | Créez un chargeur de fichier de façon asynchrone.     |
| [**D3DX10CreateAsyncMemoryLoader**](d3dx10createasyncmemoryloader.md)     | Créez un chargeur de données de façon asynchrone.     |
| [**D3DX10CreateAsyncResourceLoader**](d3dx10createasyncresourceloader.md) | Créez un chargeur de ressource de manière asynchrone. |



 

Processeurs de données D3DX10 intégrés



|                                                                                                 |  Description                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md)                   | Créez un processeur de données à utiliser avec une pompe de thread. Cette API est similaire à D3DX10CreateAsyncTextureInfoProcessor, mais elle charge également la texture. |
| [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md)           | Créez un processeur de données à utiliser avec une pompe de thread.                                                                                             |
| [**D3DX10CreateAsyncShaderCompilerProcessor**](d3dx10createasyncshadercompilerprocessor.md)     | Compilez un nuanceur et créez un processeur de données de façon asynchrone.                                                                                       |
| [**D3DX10CreateAsyncEffectCompilerProcessor**](d3dx10createasynceffectcompilerprocessor.md)     | Créer un effet avec un processeur de données de façon asynchrone.                                                                                             |
| [**D3DX10CreateAsyncEffectCreateProcessor**](d3dx10createasynceffectcreateprocessor.md)         | Créer un pool d’effets de manière asynchrone.                                                                                                              |
| [**D3DX10CreateAsyncEffectPoolCreateProcessor**](d3dx10createasynceffectpoolcreateprocessor.md) | Créer un processeur de données de façon asynchrone.                                                                                                            |
| [**D3DX10CreateAsyncShaderPreprocessProcessor**](d3dx10createasyncshaderpreprocessprocessor.md) | Créer un processeur de données pour un nuanceur de manière asynchrone.                                                                                               |



 

API qui prennent une pompe de thread comme paramètre.



|                                                                                                 | Description                                                                 |
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**D3DX10CompileFromFile**](d3dx10compilefromfile.md)                                           | Compilez un nuanceur à partir d’un fichier.                                    |
| [**D3DX10CompileFromMemory**](d3dx10compilefrommemory.md)                                       | Compilez un nuanceur résidant en mémoire.                             |
| [**D3DX10CompileFromResource**](d3dx10compilefromresource.md)                                   | Compilez un nuanceur à partir d’une ressource.                                |
| [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md)                                 | Créer un effet à partir d’un fichier.                                    |
| [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md)                             | Créez un effet à partir de la mémoire.                                    |
| [**D3DX10CreateEffectFromResource**](d3dx10createeffectfromresource.md)                         | Créer un effet à partir d’une ressource.                                |
| [**D3DX10CreateEffectPoolFromFile**](d3dx10createeffectpoolfromfile.md)                         | Créer un pool d’effets à partir d’un fichier.                               |
| [**D3DX10CreateEffectPoolFromMemory**](d3dx10createeffectpoolfrommemory.md)                     | Créer un pool d’effets à partir d’un fichier résidant en mémoire.            |
| [**D3DX10CreateEffectPoolFromResource**](d3dx10createeffectpoolfromresource.md)                 | Créer un pool d’effets à partir d’une ressource.                           |
| [**D3DX10PreprocessShaderFromFile**](d3dx10preprocessshaderfromfile.md)                         | Créer un nuanceur à partir d’un fichier sans le compiler.                |
| [**D3DX10PreprocessShaderFromMemory**](d3dx10preprocessshaderfrommemory.md)                     | Créer un nuanceur à partir de la mémoire sans le compiler.                |
| [**D3DX10PreprocessShaderFromResource**](d3dx10preprocessshaderfromresource.md)                 | Créez un nuanceur à partir d’une ressource sans le compiler.            |
| [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md)         | Créer un affichage des ressources de nuanceur à partir d’un fichier.                       |
| [**D3DX10CreateShaderResourceViewFromMemory**](d3dx10createshaderresourceviewfrommemory.md)     | Créer un affichage des ressources de nuanceur à partir d’un fichier en mémoire.             |
| [**D3DX10CreateShaderResourceViewFromResource**](d3dx10createshaderresourceviewfromresource.md) | Créer un affichage des ressources de nuanceur à partir d’une ressource.                   |
| [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md)                                 | Récupère des informations sur un fichier image donné.                  |
| [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)                             | Obtenir des informations sur une image déjà chargée en mémoire.       |
| [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md)                         | Récupère des informations sur une image donnée dans une ressource.         |
| [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)                               | Créer une ressource de texture à partir d’un fichier.                           |
| [**D3DX10CreateTextureFromMemory**](d3dx10createtexturefrommemory.md)                           | Créer une ressource de texture à partir d’un fichier résidant dans la mémoire système. |
| [**D3DX10CreateTextureFromResource**](d3dx10createtexturefromresource.md)                       | Créer une ressource de texture à partir d’une autre ressource.                 |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
