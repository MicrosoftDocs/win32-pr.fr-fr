---
description: utilisation du modèle de classe DMO
ms.assetid: 5193ad08-aaee-47e3-93eb-a126a66d8f23
title: utilisation du modèle de classe DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db80017372f11f6c928e0e6a83b591967a84ee7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857403"
---
# <a name="using-the-dmo-class-template"></a>utilisation du modèle de classe DMO

DirectShow comprend un modèle de classe, [**IMediaObjectImpl**](imediaobjectimpl-class-template.md), pour l’implémentation de DMOs. Le modèle gère un grand nombre des tâches de « comptabilité », telles que la validation des paramètres d’entrée. À l’aide du modèle, vous pouvez vous concentrer sur les fonctionnalités spécifiques à votre DMO. En outre, le modèle permet de s’assurer que vous créez une implémentation robuste. Le modèle est défini dans le fichier d’en-tête Dmoimpl. h, situé dans le répertoire include du kit de développement logiciel (SDK).

Le modèle **IMediaObjectImpl** hérite de l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) . pour créer un DMO à l’aide du modèle, définissez une nouvelle classe qui dérive de **IMediaObjectImpl**. Le modèle implémente toutes les méthodes **IMediaObject** . Dans la plupart des cas, le modèle appelle une méthode privée correspondante sur la classe dérivée. Le modèle fournit les fonctionnalités suivantes :

-   Vérification de paramètres de base. Les méthodes de modèle vérifient que les paramètres requis ne sont pas **null**, que les index de flux se trouvent dans la plage et que les indicateurs sont valides.
-   Verr. Les méthodes de modèle appellent deux méthodes internes, **Lock** et **Unlock**, pour sérialiser des opérations sur le DMO. cette fonctionnalité garantit que la DMO est thread-safe.
-   Types de médias. Le modèle stocke les types de médias définis par le client et fournit des méthodes d’accesseur pour les types de média.
-   Contenu. Le modèle empêche la diffusion en continu jusqu’à ce que le client ait défini des types de médias pour tous les flux non facultatifs. Elle garantit également que la méthode [**IMediaObject :: AllocateStreamingResources**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) est appelée avant le début de la diffusion en continu, ce qui garantit que les ressources sont allouées.

La classe dérivée doit implémenter l’interface **IUnknown** ; le modèle ne fournit pas cette interface. Vous pouvez utiliser la Active Template Library (ATL) pour implémenter **IUnknown**, ou vous pouvez fournir une autre implémentation. Le modèle n’implémente pas non plus le mécanisme de verrouillage. La classe dérivée doit implémenter les méthodes **Lock** et **Unlock** . Si vous créez votre classe à l’aide d’ATL, vous pouvez utiliser les implémentations ATL par défaut.

**Déclaration de la classe dérivée**

Le modèle de classe **IMediaObjectImpl** est déclaré comme suit :


```C++
template <class _DERIVED_, int NUMBEROFINPUTS, int NUMBEROFOUTPUTS>
class IMediaObjectImpl : public ImediaObject
```



Les trois paramètres de modèle sont \_ dérivés \_ , NUMBEROFINPUTS et NUMBEROFOUTPUTS. Définissez une valeur \_ dérivée \_ égale au nom de votre classe. Les deux autres paramètres définissent le nombre de flux d’entrée et de flux de sortie sur le DMO. par exemple, pour créer une classe DMO nommée CMyDmo qui prend en charge un flux d’entrée et deux flux de sortie, utilisez la déclaration suivante :


```C++
class CMyDmo : public IMediaObjectImpl<CMyDmo, 1, 2>
```



Le reste de cette section décrit comment le modèle implémente les différentes méthodes dans **IMediaObject**.

**Méthodes de définition des types de média**

Les méthodes suivantes définissent ou récupèrent les types de média sur le DMO :

-   **GetInputType**, **GetOutputType**. Ces méthodes retournent les types de média préférés, par numéro de flux et index de type. Le modèle appelle **InternalGetInputType** ou **InternalGetOutputType** sur la classe dérivée.
-   **SetInputType**, **SetOutputType**. Ces méthodes définissent le type de média sur un flux, testent un type de média ou effacent un type de média. Pour valider le type de média, le modèle appelle **InternalCheckInputType** ou **InternalCheckOutputType** sur la classe dérivée. la classe dérivée retourne S \_ OK pour accepter le type ou DMO \_ E \_ INVALIDTYPE pour rejeter le type. Les handles de modèle déterminent ou effacent le type de média.
-   **GetInputCurrentType**, **GetOutputCurrentType**. ces méthodes retournent le type de média actuel d’un flux, ou DMO \_ \_ type E \_ non \_ défini si aucun type n’est défini. Le modèle implémente complètement ces méthodes.

**Méthodes d’information**

Les méthodes suivantes fournissent des informations sur les DMO.

-   **GetInputMaxLatency**, **SetInputMaxLatency**. Ces méthodes récupèrent ou définissent la latence maximale. Le modèle appelle **InternalGetInputMaxLatency** ou **InternalSetInputMaxLatency** sur la classe dérivée.
-   **GetInputSizeInfo**, **GetOutputSizeInfo**. ces méthodes retournent les exigences de mémoire tampon de DMO pour un flux spécifié. si aucun type de support n’a été défini sur ce flux, le modèle retourne DMO \_ \_ type E \_ non \_ défini. Sinon, elle appelle **InternalGetInputSizeInfo** ou **InternalGetOutputSizeInfo** sur la classe dérivée.
-   **GetInputStreamInfo**, **GetOutputStreamInfo**. Ces méthodes retournent différents indicateurs qui indiquent comment le client doit mettre en forme les données. Le modèle appelle **InternalGetInputStreamInfo** ou **InternalGetOutputStreamInfo** sur la classe dérivée.
-   **GetStreamCount**. Cette méthode retourne le nombre de flux d’entrée et de sortie. Le modèle implémente cette méthode, à l’aide des paramètres du modèle.

**Méthodes d’allocation des ressources**

-   la méthode **AllocateStreamingResources** alloue toutes les ressources dont le DMO a besoin avant le début de la diffusion en continu. La méthode **FreeStreamingResources** libère les mêmes ressources. Le modèle appelle **InternalAllocateStreamingResources** et **InternalFreeStreamingResources**, respectivement.

le client de l’DMO n’est pas obligé d’appeler ces méthodes, mais le modèle appelle automatiquement **AllocateStreamingResources** avant le démarrage de la diffusion en continu. par conséquent, l’DMO peut supposer que les ressources ont été allouées correctement lors de l’appel de **ProcessInput** . le DMO doit appeler **FreeStreamingResources** dans son destructeur.

En outre, lorsque le modèle appelle **InternalAllocateStreamingResources**, il définit un indicateur interne, afin qu’il n’appelle pas à nouveau cette méthode avant d’appeler **InternalFreeStreamingResources**. Cela permet de s’assurer que les ressources ne sont pas réallouées accidentellement, ce qui peut provoquer des fuites de mémoire.

**Méthodes pour la diffusion en continu**

Les méthodes suivantes sont utilisées pour diffuser des données en continu :

-   **GetInputStatus**. cette méthode indique si la DMO peut accepter l’entrée pour l’instant. Le modèle appelle **InternalAcceptingInput** sur la classe dérivée. si la DMO peut accepter une entrée, la classe dérivée retourne la valeur S \_ OK et le modèle définit le \_ bit d’entrée de DMO \_ STATUSF \_ accept \_ de données dans le paramètre *dwFlags* . Sinon, la classe dérivée retourne S \_ false et le modèle affecte la valeur zéro à *dwFlags* .
-   **ProcessInput**. Cette méthode traite une mémoire tampon d’entrée. Le modèle appelle **AllocateStreamingResources**, décrit précédemment. Il appelle ensuite **InternalAcceptingInput** sur la classe dérivée. si le DMO peut accepter une nouvelle entrée, le modèle appelle **InternalProcessInput**.
-   **ProcessOutput**. Cette méthode traite un jeu de mémoires tampons de sortie, une mémoire tampon pour chaque flux de sortie. Le modèle appelle **AllocateStreamingResources** , puis **InternalProcessOutput**.
-   **Discontinuation**. Cette méthode signale une discontinuité dans un flux d’entrée. Le modèle appelle **InternalAcceptingInput** sur la classe dérivée. Si cette méthode retourne \_ la valeur OK, le modèle appelle **InternalDiscontinuity** sur la classe dérivée.
-   **Vidage**. Cette méthode vide le DMO. Le modèle appelle **InternalFlush** sur la classe dérivée. le DMO doit ignorer les tampons d’entrée qu’il détient toujours pour être traité.

Le modèle ne fournit pas de prise en charge directe de l’interface [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) .

**Méthodes de verrouillage**

le verrouillage est utilisé pour protéger l’état de l’DMO dans un environnement multithread. Dans un projet ATL, la méthode [**IMediaObject :: Lock**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-lock) provoque un conflit de nom avec la méthode de **verrouillage** ATL. Pour résoudre le conflit, le modèle renomme la méthode **IMediaObject** en **DMOLock**. Quand vous compilez la classe dérivée, définissez corriger le \_ \_ nom du verrou avant d’inclure le fichier d’en-tête DMO. h :


```C++
#define FIX_LOCK_NAME
#include <dmo.h>
```



Cette directive force le préprocesseur à substituer **DMOLock** pour le **verrou** dans la déclaration de l’interface **IMediaObject** . Les applications peuvent toujours appeler la méthode à l’aide du **verrou** de nom, car l’ordre vtable ne change pas. La méthode **DMOLock** appelle **Lock** ou **Unlock** sur la classe dérivée. Si vous utilisez ATL pour implémenter la classe dérivée, ces méthodes sont déjà définies par ATL, donc aucun code supplémentaire n’est nécessaire. Si vous n’utilisez pas ATL, vous devez fournir des méthodes de **verrouillage** et de **déverrouillage** dans votre classe dérivée.

le modèle verrouille automatiquement les DMO dans chacune des méthodes **IMediaObject** . la classe dérivée peut être amenée à verrouiller le DMO à l’intérieur d’autres méthodes publiques qu’il implémente (par exemple, s’il prend en charge **IMediaObjectInPlace**). Le modèle de classe fournit également une classe d’assistance interne, [**IMediaObjectImpl :: LockIt**](imediaobjectimpl-lockit.md), qui est utile pour le verrouillage et le déverrouillage du DMO.

**Résumé**

Pour les méthodes **IMediaObject** suivantes, le modèle appelle une méthode correspondante avec la même signature sur la classe dérivée. La classe dérivée doit implémenter chacune des méthodes indiquées dans la deuxième colonne.



| Méthode IMediaObject            | Méthode de classe dérivée                   |
|--------------------------------|----------------------------------------|
| **AllocateStreamingResources** | **InternalAllocateStreamingResources** |
| **Discontinuité**              | **InternalDiscontinuity**              |
| **Purge**                      | **InternalFlush**                      |
| **FreeStreamingResources**     | **InternalFreeStreamingResources**     |
| **GetInputMaxLatency**         | **InternalGetInputMaxLatency**         |
| **GetInputSizeInfo**           | **InternalGetInputSizeInfo**           |
| **GetInputStreamInfo**         | **InternalGetInputStreamInfo**         |
| **GetInputType**               | **InternalGetInputType**               |
| **GetOutputSizeInfo**          | **InternalGetOutputSizeInfo**          |
| **GetOutputStreamInfo**        | **InternalGetOutputStreamInfo**        |
| **GetOutputType**              | **InternalGetOutputType**              |
| **ProcessInput**               | **InternalProcessInput**               |
| **ProcessOutput**              | **InternalProcessOutput**              |
| **SetInputMaxLatency**         | **InternalSetInputMaxLatency**         |



 

Pour les méthodes **IMediaObject** restantes, il n’existe pas de correspondance un-à-un entre les méthodes de modèle et les méthodes de classe dérivée. Le tableau suivant résume les méthodes qui sont entièrement implémentées par le modèle, et les méthodes qui appellent d’autres méthodes sur la classe dérivée.



| Méthode IMediaObject                   | Méthode de classe dérivée                                                             |
|---------------------------------------|----------------------------------------------------------------------------------|
| **GetInputCurrentType**               | Entièrement implémentée                                                                |
| **GetOutputCurrentType**              | Entièrement implémentée                                                                |
| **GetStreamCount**                    | Entièrement implémentée                                                                |
| **GetInputStatus**                    | [**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))        |
| **Verrou** (implémenté en tant que **DMOLock**) | [**Verrouillage**](/previous-versions/ms809100(v=msdn.10)), [ **déverrouillage**](/previous-versions/ms809101(v=msdn.10)) |
| **SetInputType**                      | [**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))        |
| **SetOutputType**                     | [**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10))      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Modèle de classe IMediaObjectImpl**](imediaobjectimpl-class-template.md)
</dt> <dt>

[Écriture d’un DMO](writing-a-dmo.md)
</dt> </dl>

 

 
