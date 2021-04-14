---
description: Les questions fréquemment posées (FAQ) sur le développement des composants de plateforme Tablet PC installés par le kit de développement logiciel (SDK) Windows Vista sont les suivantes.
ms.assetid: eb349493-a2b2-4b58-bcbc-ee09953c8dc8
title: Forum aux questions (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8722c00fa5aaf2b43494484fc015fa8b3e4c7826
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104383447"
---
# <a name="frequently-asked-questions-about-developing-for-the-tablet-pc-platform"></a>Forum aux questions sur le développement pour la plateforme Tablet PC

Les questions fréquemment posées (FAQ) sur le développement des composants de plateforme Tablet PC installés par le kit de développement logiciel (SDK) Windows Vista sont les suivantes.

## <a name="q-can-i-use-the-ink-apis-or-controls-in-a-web-page"></a>Q. Puis-je utiliser les API ou les contrôles Ink dans une page Web ?

R. Oui. La bibliothèque gérée Tablet PC prend en charge des environnements de confiance partielle, à savoir l’exécution d’assemblys managés à partir de pages Web.

Il existe également une prise en charge pour le déploiement de navigateurs d’applications qui utilisent Windows Presentation Foundation.

## <a name="q-do-i-need-a-tablet-pc-to-develop-tablet-pc-applications"></a>Q. Ai-je besoin d’un Tablet PC pour développer des applications Tablet PC ?

R. Non, les composants de plateforme Tablet PC installés par le SDK Windows incluent les extensions et les utilitaires nécessaires au développement de logiciels pour Tablet PC sur un ordinateur de bureau ou portable. Vous pouvez utiliser une souris ou une tablette externe pour l’entrée de stylet et d’écriture manuscrite.

Les composants de plateforme Tablet PC installés par le SDK Windows peuvent être installés sur Windows XP professionnel ou Windows Server 2003, mais les fonctionnalités sont moins disponibles pour vos applications. Sur ces plateformes, votre application peut collecter de l’encre avec les objets [**InkCollector**](inkcollector-class.md) et [**InkOverlay**](inkoverlay-class.md) et peut être testée et déboguée.

En outre, les contrôles [InkEdit](inkedit-control-reference.md) et [InkPicture](inkpicture-control-reference.md) peuvent collecter de l’encre sur ces systèmes d’exploitation uniquement si les composants de plateforme Tablet PC ont été installés à partir du SDK Windows (ou d’une version antérieure du kit de développement Tablet PC). ils ne recueillent pas d’encre dans les applications qui sont redistribuées sur des ordinateurs non-tablettes sans que les composants de plateforme soient installés.

## <a name="q-do-i-need-to-run-a-special-version-of-windows-to-do-handwriting-recognition"></a>Q. Dois-je exécuter une version spéciale de Windows pour la reconnaissance de l’écriture manuscrite ?

R. Non. Bien que seul Windows XP Édition Tablet PC et certaines versions de Windows Vista incluent des modules de reconnaissance de l’écriture manuscrite, vous pouvez télécharger le [Pack de reconnaissance de Windows XP Édition Tablet pc 2005]( https://www.microsoft.com/downloads/details.aspx?FamilyId=080184DD-5E92-4464-B907-10762E9F918B&amp;displaylang=en) et l’installer sur Windows XP professionnel ou windows Server 2003 à des fins de développement uniquement. Vous ne pouvez pas redistribuer les module de reconnaissance avec votre application.

## <a name="q-what-is-the-difference-between-windows-vista-and-tablet-pc-technology"></a>Q. Quelle est la différence entre les technologies Windows Vista et Tablet PC ?

R. Les Tablet PC exécutent le système d’exploitation Windows Vista, avec toutes les fonctionnalités de Windows Vista, ainsi que des fonctionnalités supplémentaires spécifiques au Tablet PC. Ces fonctionnalités de la technologie Tablet PC permettent aux utilisateurs d’exécuter des applications Windows et Windows à l’aide d’un stylet, d’annoter des documents et de créer des documents manuscrits à l’aide d’une encre numérique. La technologie Tablet PC est disponible sur la plupart des versions de Windows Vista, et si le matériel du Tablet PC est disponible sur un ordinateur, les fonctionnalités fonctionnent.

Pour les versions antérieures des systèmes d’exploitation Windows qui ne prennent pas en charge l’encre en mode natif, vous pouvez redistribuer et utiliser les contrôles d’encre du Tablet PC pour afficher l’encre dessinée sur un Tablet PC.

## <a name="q-what-is-the-difference-between-windows-xp-tablet-pc-edition-and-windows-xp-tablet-pc-edition-2005"></a>Q. Quelle est la différence entre Windows XP Édition Tablet PC et Windows XP Édition Tablet PC 2005 ?

R. Windows XP Édition Tablet PC 2005 est une version mise à jour de Windows XP Édition Tablet PC.

## <a name="q-how-do-i-modify-my-application-to-run-on-a-tablet-pc"></a>Q. Comment faire modifier mon application pour qu’elle s’exécute sur un Tablet PC ?

R. Les applications Microsoft Windows qui s’exécutent sur un ordinateur de bureau ou portable Windows XP avec un matériel comparable peuvent s’exécuter sur un Tablet PC sans modification.

## <a name="q-i-understand-that-i-dont-need-to-make-any-changes-to-my-application-but-it-is-difficult-to-use-it-with-a-pen-and-speech-what-can-i-do-to-optimize-my-application-for-a-tablet-pc"></a>Q. Je comprends que je n’ai pas besoin d’apporter des modifications à mon application, mais il est difficile de l’utiliser avec un stylet et une reconnaissance vocale. Que puis-je faire pour optimiser mon application pour un Tablet PC ?

R. Les contrôles d’API et d’encre des composants de la plateforme Tablet PC peuvent être utilisés pour créer des interfaces utilisateur mieux adaptées à l’entrée de stylet et de l’écriture manuscrite. Pour plus d’informations sur la façon dont vous pouvez améliorer votre application, consultez [instructions relatives à l’expérience utilisateur des ordinateurs portables pour les développeurs](/previous-versions//dd356056(v=vs.85)).

## <a name="q-what-programming-languages-does-the-tablet-support"></a>Q. Quels langages de programmation la tablette prend-elle en charge ?

R. La technologie Tablet PC de Windows Vista prend en charge les bibliothèques COM (C++) et managées (la suite de langages Visual Studio .NET).

La technologie Tablet PC prend également en charge les Windows Presentation Foundation (WPF).

## <a name="q-do-i-have-sample-code-that-demonstrates-tablet-platform-capabilities"></a>Q. Ai-je des exemples de code qui illustrent les fonctionnalités de plateforme de tablette ?

R. Oui, l’exemple de code pour COM et les langages managés sélectionnés est inclus dans les composants de plateforme Tablet PC installés par le kit de développement logiciel (SDK) de plateforme Windows.

Pour obtenir des exemples d’applications disponibles, consultez :

- [Exemples pour ordinateurs portables et Tablet PC](mobile-pc-and-tablet-pc-samples.md)
- [Exemples d’encre numérique, Windows Presentation Foundation (WPF)](/previous-versions/dotnet/netframework-3.0/aa972145(v=vs.85))
- <systemdrive>: \\ Program Files \\ Microsoft Kits SDK \\ Windows \\ v 6.0 \\ Samples \\ TabletPC

## <a name="q-whats-the-base-level-of-tablet-hardware-that-i-should-develop-for"></a>Q. Quel est le niveau de base du matériel de tablette que je dois développer pour ?

R. En général, vous devez concevoir un système Windows Vista conforme à la version antérieure.

## <a name="q-what-user-interface-guidelines-can-you-provide-for-tablet-applications"></a>Q. Quelles instructions de l’interface utilisateur pouvez-vous fournir pour les applications Tablet ?

R. Les problèmes de l’orientation du menu déroulant à la parallaxe de l’écran/du digitaliseur sont décrits dans la section Guide de l' [expérience utilisateur des ordinateurs portables pour les développeurs](/previous-versions//dd356056(v=vs.85)) dans la section ordinateur portable de la SDK Windows.

## <a name="q-do-you-include-system-level-handwriting-gestures-for-commonly-used-keystrokes-can-i-create-my-own-gestures-for-use-when-an-application-is-running-or-has-focus"></a>Q. Incluez-vous des gestes d’écriture au niveau du système pour les séquences de touches couramment utilisées ? Puis-je créer mes propres gestes à utiliser lorsqu’une application est en cours d’exécution ou a le focus ?

R. Oui, nous incluons un ensemble de mouvements pour les événements de souris. En outre, vous pouvez créer des gestes à utiliser dans votre application. Pour plus d’informations sur les gestes, consultez [utilisation des mouvements](using-gestures.md).

## <a name="q-how-can-i-determine-whether-my-application-is-running-on-a-tablet"></a>Q. Comment puis-je déterminer si mon application s’exécute sur une tablette ?

R. Utilisez le GetSystemMetricsAPI Windows et transmettez le SM \_ TABLETPC comme valeur de l’index. SM \_ TABLETPC est défini dans winuser. h. La valeur de SM \_ TABLETPC est 86.

Pour le développement Web, vous devez lire la \_ variable d’environnement de la chaîne de l’agent utilisateur \_ . Vous pouvez accéder à cette collection Request. ServerVariables.

Pour plus d’informations sur l’utilisation de GetSystemMetrics sur les Tablet PC exécutant Windows Vista ou Windows XP Édition Tablet PC, reportez-vous à [déterminer si un PC est un Tablet PC](determining-whether-a-pc-is-a-tablet-pc.md).

## <a name="q-how-can-i-determine-whether-tablet-platform-components-are-available"></a>Q. Comment puis-je déterminer si des composants de plateforme tablette sont disponibles ?

R. Certaines parties de la plateforme Tablet PC peuvent être installées sur des versions non-Tablet des systèmes d’exploitation Windows XP professionnel, Windows Server 2003 et Windows 2000.

Pour déterminer si un composant de l’API est installé, la méthode appropriée consiste à tenter de créer une instance d’un objet ou d’un contrôle et à vérifier qu’il existe avant de tenter de l’utiliser.

Par exemple, pour déterminer si l’objet [**InkCollector**](inkcollector-class.md) est disponible, essayez de le créer à l’aide de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

```C++
IInkCollector* pIInkCollector = NULL;
HRESULT hr = CoCreateInstance(CLSID_InkCollector,
 NULL, CLSCTX_INPROC_SERVER, 
 IID_IInkCollector,
 (void **)&pIInkCollector);
if (SUCCEEDED(hr)) 
{ 
  /* InkCollector is usable. */ 
} else 
{
  /* InkCollector unavailable. */
}
```

## <a name="q-how-do-i-run-the-tablet-input-service-on-server-skus"></a>Q. Comment faire exécuter le service d’entrée de tablette sur les références de serveur ?

R. TabletInputService est conçu pour ne pas s’exécuter automatiquement dans les références de serveur lors de l’installation du Pack client. Le Pack client installe tous les composants de la plateforme, de sorte que toutes les applications clientes de tablette peuvent également s’exécuter sur un serveur. Le service d’entrée de tablette écoute la notification PnP qu’un digitaliseur externe est branché. Pour activer le service d’entrée de tablette sur un serveur, utilisez l’utilitaire de configuration système.

Dans le menu **Démarrer** , sélectionnez **exécuter**. Tapez « msconfig », puis appuyez sur entrée. Sélectionnez l’onglet **services** , recherchez les services nommés « service d’entrée HID », activez la case à cocher en regard, puis cliquez sur **appliquer**. Fermez l’utilitaire.

## <a name="q-more-faqs-and-other-resources"></a>Q. Autres questions fréquentes et autres ressources

- [Centre de développement Microsoft](https://developer.microsoft.com)
- [Référence du Tablet PC de base](./core-reference---tablet-pc-com-library.md)