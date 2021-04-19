---
description: Les classes WMI C++ qui font partie de l’infrastructure du fournisseur WMI ne sont plus recommandées pour une utilisation.
ms.assetid: d2414a72-3435-4035-bcd9-b3ec87f5709c
ms.tgt_platform: multiple
title: Classes de l’utilitaire de l’infrastructure du fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab09c99fe2597cacd81e55a4ed18bd4e286ff16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521982"
---
# <a name="provider-framework-utility-classes"></a>Classes de l’utilitaire de l’infrastructure du fournisseur

\[Les classes WMI C++ qui font partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucun développement, amélioration ou mise à jour supplémentaire n’est disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

Les bibliothèques de l’infrastructure du fournisseur Framedyd.dll (version de débogage) et Framedyn.dll (version Release) implémentent plusieurs classes d’assistance de fournisseur. Certaines fonctions de Framedyn.dll ont été supprimées des fichiers d’en-tête. Pour continuer à utiliser ces fonctions, ajoutez `#define FRAMEWORK_ALLOW_DEPRECATED` à votre code avant d’inclure Fwcommon. h.

Vous pouvez décharger des fournisseurs individuels qui ne sont plus nécessaires.

Pour utiliser cette fonctionnalité, vous devez apporter les trois modifications suivantes à votre fournisseur dans MainDll. cpp :

-   Dans la fonction **DllMain** où vous appelez [**CWbemProviderGlue :: FrameworkLoginDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong)), vous devez ajouter un deuxième paramètre qui est un pointeur vers une valeur long.
-   Dans la fonction **DllCanUnloadNow** où vous appelez [**CWbemProviderGlue :: FrameworkLogoffDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong)), vous devez ajouter un deuxième paramètre qui est un pointeur vers une valeur long.
-   Dans la fonction **DllGetClassObject** dans laquelle vous créez une instance de **CWbemGlueFactory**, vous devez ajouter un paramètre qui est un pointeur vers une valeur long.

Dans les trois cas, le pointeur vers long doit être le même pointeur.

> [!Note]  
> Dans mainDLL. cpp, les routines **DllGetClassObject**, **DllCanUnloadNow**, **DllRegisterServer**, **DllUnregisterServer** et **DllMain** doivent être encapsulées dans un bloc try/catch.

 

> [!Caution]  
> Les builds de débogage de fournisseur sont liées à Framedyd. lib pour Framedyd.dll. Framedyd.dll se trouve dans le répertoire bin du kit de développement logiciel (SDK) Microsoft Windows \\ qui n’est pas inclus dans le chemin d’accès système. Quand une version Debug d’un fournisseur est testée avec le service de gestion Windows, le chargement du fournisseur Framework échoue car Framedyd.dll ou l’une de ses dépendances ne sera pas trouvé. Par conséquent, vous devez copier Framedyd.dll à partir du \\ répertoire SDK Windows bin vers \\ le \\ répertoire system32 wbem ou ajouter le \\ répertoire SDK Windows bin au chemin de recherche du système.

 

Le tableau suivant répertorie les classes de l’utilitaire de l’infrastructure du fournisseur.



| Classe utilitaire                                          | Description                                                                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**CHString**](chstring.md)                           | Fournit des fonctions de comparaison et de manipulation de chaînes pour WMI.                                                                  |
| [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray)                 | Contient pour la création et la manipulation de tableaux de CHString.                                                                      |
| [**TRefPointerCollection**](/windows/desktop/api/RefPtrCo/nl-refptrco-trefpointercollection) | Accorde l’accès à une classe de conteneur pour les pointeurs.                                                                                |
| [**WBEMTime**](wbemtime.md)                           | Facilite les conversions entre les différents formats d’heure d’exécution de Windows et ANSI C.                                               |
| [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan)                   | Contient des fonctions d’assistance utilisées pour calculer et conserver la différence de temps entre deux objets [**WBEMTime**](wbemtime.md) . |



 

> [!Note]  
> Les classes [**CHString**](chstring.md) et [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) sont similaires à la Microsoft Foundation classes (MFC) **CString** et à **CStringArray**. Les versions de WMI existent pour permettre aux développeurs d’accéder à des méthodes de comparaison et de manipulation de chaînes sans avoir à accéder aux MFC. Les classes [**WBEMTime**](wbemtime.md) et [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) sont également similaires aux classes MFC **ctime** et **CTimeSpan** . Les versions WMI sont capables de stocker la précision de la durée de la nanoseconde et peuvent également être converties vers et à partir de **BSTR**. Pour plus d’informations sur les classes CString, CStringArray, CTime et CTimeSpan, consultez les [Microsoft Foundation classes](https://msdn.microsoft.com/library/d06h2x6e(VS.71).aspx) sur MSDN.

 

Les valeurs **BSTR** retournées par les méthodes [**WBEMTime**](wbemtime.md) sont au [format de date et d’heure](date-and-time-format.md): « AAAAMMJJHHMMSS. mmmmmmsUUU »

Les valeurs **BSTR** retournées par les méthodes [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) sont au [format d’intervalle](interval-format.md): « ddddddddHHMMSS. mmmmmm : 000 »

Bien que les heures et les intervalles de temps soient stockés en interne en tant que nanosecondes, ils ne sont pas nécessairement stockés avec une précision de nanoseconde. Cela est dû au fait que les objets [**WBEMTime**](wbemtime.md) peuvent être construits à l’aide de formats d’heure précis à une seconde (**struct TM** et **Time \_ t**). L’ajout de décimales artificielles n’augmente pas la précision.

 

 
