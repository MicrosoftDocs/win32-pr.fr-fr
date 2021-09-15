---
description: Explique comment créer un contrôle d’entrée mathématique.
ms.assetid: 59976b01-9032-4226-a160-e9b2d4b8b23b
title: Création d’un contrôle d’entrée mathématique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5084f29943395bc6781fe20598f86bdc08c6c61
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294662"
---
# <a name="creating-a-math-input-control"></a>Création d’un contrôle d’entrée mathématique

Pour créer le contrôle d’entrée mathématique, vous devez :

-   [Inclure des en-têtes et des bibliothèques pour le contrôle d’entrée mathématique](#include-headers-and-libraries-for-the-math-input-control)
-   [Déclarer le pointeur de contrôle et appeler CoInitialize sur le pointeur de contrôle](#declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer)
-   [Afficher le contrôle](#show-the-control)

## <a name="include-headers-and-libraries-for-the-math-input-control"></a>Inclure des en-têtes et des bibliothèques pour le contrôle d’entrée mathématique

Le code suivant doit être placé en haut de votre code où vous utiliserez le contrôle d’entrée mathématique.


```
   // includes for implementation
   #include "micaut.h"
   #include "micaut_i.c"
   
```



Ce code ajoute la prise en charge du contrôle d’entrée mathématique à votre application.

## <a name="declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer"></a>Déclarer le pointeur de contrôle et appeler CoInitialize sur le pointeur de contrôle

Une fois que vous avez inclus les en-têtes pour votre contrôle, vous pouvez déclarer le pointeur de contrôle et vous pouvez appeler CoInitialize dessus pour créer un handle pour l’interface de contrôle d’entrée mathématique. Le code suivant peut être placé dans une classe ou en tant que variable globale dans l’implémentation de votre application :


```
   CComPtr<IMathInputControl> g_spMIC; // Math Input Control
   
```



Le code suivant montre comment appeler CoInitialize sur le pointeur de contrôle.


```
   HRESULT hr = CoInitialize(NULL);
   hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
   
```



Après avoir appelé CoInitialize sur le pointeur de contrôle, vous disposez d’une référence au contrôle et vous pouvez accéder aux méthodes du contrôle. Par exemple, vous pouvez activer l’ensemble étendu de contrôles comme indiqué dans l’exemple suivant.


```
   hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
   
```



## <a name="show-the-control"></a>Afficher le contrôle

Le contrôle ne s’affiche pas automatiquement une fois que vous l’avez créé. Pour afficher le contrôle, appelez la méthode [**Show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) sur la référence de contrôle que vous avez créée à l’étape précédente. Le code suivant montre comment la méthode [**Show**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) peut être appelée.


```
   hr = g_spMIC->Show();
   
```



Une fois que le contrôle s’affiche, il ressemble à l’illustration suivante.

![capture d’écran montrant le contrôle d’entrée mathématique](images/mic.png)

Notez que j’ai activé le jeu de boutons étendus pour que les opérations de **restauration par progression** et les **annulations** soient disponibles.

 

 
