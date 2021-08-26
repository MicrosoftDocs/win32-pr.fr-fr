---
description: 'En savoir plus sur : définition de la prise en forme PPP par défaut pour un processus'
title: Définition de la reconnaissance par défaut des PPP pour un processus (Windows)
TOCTitle: Setting the default DPI awareness for a process
ms:assetid: C9488338-D863-45DF-B5CB-7ED9B869A5E2
ms:mtpsurl: https://msdn.microsoft.com/library/Mt846517(v=VS.85)
ms:contentKeyID: 74520139
ms.date: 03/30/2018
ms.topic: article
mtps_version: v=VS.85
ms.openlocfilehash: 216952ac05811226c403739d389f8de9f636c3b8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880527"
---
# <a name="setting-the-default-dpi-awareness-for-a-process"></a>Définition de la reconnaissance par défaut des PPP pour un processus

les applications de bureau sur Windows peuvent s’exécuter dans différents modes de reconnaissance ppp. Ces modes activent différents comportements de mise à l’échelle DPI et peuvent utiliser des espaces de coordonnées différents. Pour plus d’informations sur la reconnaissance DPI, consultez [développement d’applications bureautiques haute résolution sur Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\)) Il est important de définir explicitement le mode de reconnaissance PPP par défaut de votre processus afin d’éviter tout comportement inattendu.

Il existe deux méthodes principales pour spécifier la prise en compte des PPP par défaut d’un processus :

1 \) via un paramètre du manifeste d’application

2 par \) programmation à l’aide d’un appel d’API

Nous vous recommandons de spécifier la reconnaissance par défaut des PPP de processus via un paramètre de manifeste. Si la spécification de l’API par défaut via est prise en charge, elle n’est pas recommandée.

## <a name="setting-default-awareness-with-the-application-manifest"></a>Définition de la sensibilisation par défaut au manifeste d’application

Il existe deux paramètres de manifeste qui vous permettent de spécifier le mode de reconnaissance PPP par défaut du processus : \<dpiAwareness\> et \<dpiAware\> . \<dpiAware\>a été introduite dans Windows Vista et permet uniquement de définir la reconnaissance du système par défaut de votre processus. \<dpiAwareness\>a été introduite dans Windows 10, version 1607 et vous permet de spécifier une liste triée de modes de reconnaissance des ppp par défaut de processus. cela vous permet de définir les modes de reconnaissance ppp de sauvegarde, qui seront utilisés si votre application est exécutée sur une version de Windows ne peut pas prendre en charge le premier mode de sensibilisation spécifié. dans les versions antérieures de Windows, la \<dpiAwareness\> balise la plus récente sera ignorée. cela signifie que vous pouvez utiliser ces deux paramètres de manifeste pour activer un scénario dans lequel la valeur par défaut du processus peut être la reconnaissance du système sur une version antérieure de Windows tout en étant Per-Monitor sur les versions supérieures à Windows 10, version 1607. sur Windows 10, la version 1607 et la valeur on, le \<dpiAware\> paramètre est ignoré si l' \<dpiAwareness\> élément est présent.

Le tableau ci-dessous montre comment spécifier des modes de reconnaissance des PPP par défaut de processus différents à l’aide des deux paramètres de manifeste :


| Traiter le mode de reconnaissance PPP par défaut | &lt;&gt;paramètre dpiAware | &lt;&gt;paramètre dpiAwareness (Windows 10, version 1607 et versions ultérieures) | 
|------------------------------------|--------------------|--------------------------------------------------------------|
| ignore | <p>N/A (aucun paramètre dpiAware dans le manifeste)</p><p>ou</p><p>&lt;dpiAware &gt; false &lt; /dpiAware&gt;</p> | &lt;dpiAwareness ne &gt; connaissant pas &lt; /dpiAwareness&gt; | 
| Prise en charge par le système | &lt;dpiAware &gt; true &lt; /dpiAware&gt; | &lt;dpiAwareness &gt; système &lt; /dpiAwareness&gt; | 
| Par moniteur | &lt;dpiAware &gt; true/PM &lt; dpiAware&gt; | &lt;dpiAwareness &gt; permonitor &lt; /dpiAwareness&gt; | 
| Par moniteur v2 | Non prise en charge | &lt;dpiAwareness &gt; PerMonitorV2 &lt; /dpiAwareness&gt; | 


 

L’exemple ci-dessous montre à la fois les \<dpiAwareness\> \<dpiAware\> paramètres et utilisés dans le même fichier manifeste pour configurer le comportement de reconnaissance dpi par défaut du processus pour les différentes versions de Windows.

```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
  <asmv3:application>
    <asmv3:windowsSettings>
      <dpiAware xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">true</dpiAware>
      <dpiAwareness xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">PerMonitorV2</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

## <a name="setting-default-awareness-programmatically"></a>Définition par programmation de la sensibilisation par défaut

Bien qu’il ne soit pas recommandé, il est possible de définir la reconnaissance par défaut des PPP par défaut. Une fois qu’une fenêtre (HWND) a été créée dans votre processus, la modification du mode de reconnaissance PPP n’est plus prise en charge. Si vous définissez le mode de prise en forme des PPP par défaut du processus par programme, vous devez appeler l’API correspondante avant la création de tous les HWND.

Il existe plusieurs API qui vous permettent de spécifier la prise en compte des PPP par défaut pour votre processus. L’API actuellement recommandée est [**SetProcessDpiAwarenessContext**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\)), car les anciennes API offrent moins de fonctionnalités.

 


| API | Version minimale de Windows | Prise en charge de DPI | Prise en charge DPI système | Prise en charge DPI par moniteur | 
|-----|----------------------------|-------------|------------------|-----------------------|
| <a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDPIAware</a> | Windows Vista | N/A | SetProcessDPIAware() | N/A | 
| <a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a> | Windows 8.1 | SetProcessDpiAwareness (PROCESS_DPI_UNAWARE) | SetProcessDpiAwareness (PROCESS_SYSTEM_DPI_AWARE) | SetProcessDpiAwareness (PROCESS_PER_MONITOR_DPI_AWARE) | 
| <a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a> | Windows 10, version 1607 | SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_UNAWARE) | SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_SYSTEM_AWARE) | <p>SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</p><p>SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</p> | 


 

## <a name="process-default-vs-thread-default"></a>Processus-par défaut par rapport au thread par défaut

Ce document fait référence à la définition de la prise en face PPP par défaut pour votre processus. cela est dû au fait que Windows 10 a introduit la prise en charge de l’exécution de plusieurs modes de reconnaissance dpi au sein d’un même processus (avant Windows 10, l’ensemble du processus devait se conformer à un seul mode de reconnaissance ppp). La prise en charge de l’exécution de plusieurs modes de reconnaissance DPI au sein d’un processus est appelée « mise à l’échelle DPI en mode mixte ». Lors de l’utilisation de la mise à l’échelle DPI en mode mixte au sein de votre processus, chaque fenêtre de niveau supérieur peut s’exécuter dans un mode de reconnaissance PPP qui peut être différent de celui de la valeur par défaut du processus. Sauf spécification explicite, chaque thread utilise par défaut le processus par défaut lors de sa création. Pour plus d’informations sur la mise à l’échelle DPI en mode mixte, reportez-vous à l’article sur la mise à l' [échelle dpi en mode mixte](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) .
