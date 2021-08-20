---
title: Scripts personnalisés RAS
description: Les développeurs peuvent créer une DLL de script personnalisé qui réside sur un ordinateur client RAS. Cette DLL peut communiquer avec le serveur au cours du processus d’établissement d’une connexion.
ms.assetid: c27b8b02-6018-4441-a355-1fb890b9001c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66ac0bd83b8d7c48ee8b0468d89a70d19a5e5e6555b9a8bc8ac86d66c8cd666e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673279"
---
# <a name="ras-custom-scripting"></a>Scripts personnalisés RAS

Les développeurs peuvent créer une DLL de script personnalisé qui réside sur un ordinateur client RAS. Cette DLL peut communiquer avec le serveur au cours du processus d’établissement d’une connexion.

**Windows NT :** Les scripts personnalisés ne sont pas disponibles.

## <a name="setting-up-the-dll"></a>Configuration de la DLL

Pour configurer la DLL, créez une valeur portant le nom **CustomScriptDllPath** sous la clé de Registre suivante :

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
```

Cette valeur doit être de type **reg \_ expand \_ SZ**. La valeur doit contenir le chemin d’accès à la DLL de script personnalisé. Une seule DLL de script personnalisé est prise en charge pour chaque ordinateur client RAS.

## <a name="interaction-between-the-server-ras-and-the-custom-scripting-dll"></a>Interaction entre le serveur, RAS et la DLL Custom-Scripting

La DLL de script personnalisé doit exporter un point d’entrée unique : [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn). RAS appelle cette fonction lors de l' \_ État interactif RASCS du processus de connexion. L' \_ État interactif RASCS est un état suspendu, qui permet à l’utilisateur d’interagir avec une interface utilisateur présentée par la dll de script personnalisé. Pour plus d’informations sur les États de connexion, consultez [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) .

RAS passera comme paramètres à la fonction [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) :

-   Handle vers le port sur l’ordinateur client utilisé pour la connexion.
-   Chaînes qui identifient l’annuaire téléphonique et l’entrée pour la connexion.
-   RAS transmet également un handle à une fenêtre pour permettre à la DLL de présenter une interface utilisateur.
-   Ensemble de pointeurs de fonction que la DLL peut utiliser pour communiquer avec le serveur.

Pour plus d’informations sur ces paramètres, consultez [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) .

RAS passe un pointeur vers une structure [**RASCUSTOMSCRIPTEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa376738(v=vs.85)) comme dernier paramètre à [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn). Cette structure contient un pointeur vers une fonction de type [**PFNRASSETCOMMSETTINGS**](/windows/desktop/api/Ras/nc-ras-pfnrassetcommsettings). La DLL de script personnalisé appelle cette fonction pour modifier les paramètres de communication sur le port utilisé par la connexion.

RAS sert d’intermédiaire pour l’interaction entre le serveur et la DLL de script personnalisé. En règle générale, le serveur lance la boîte de dialogue. Par exemple, le serveur peut demander le nom d’utilisateur et le mot de passe de l’utilisateur.

lorsque vous utilisez des scripts personnalisés pour établir une connexion, le serveur n’a pas besoin d’être en cours d’exécution Windows NT 4,0 ou Windows 2000.

## <a name="custom-scripting-user-interface-must-support-idcancel"></a>L’interface utilisateur de script personnalisé doit prendre en charge IDCANCEL

Si le numéroteur personnalisé affiche une interface utilisateur, l’interface utilisateur doit prendre en charge les \_ messages de commande WM où LOWORD (*wParam*) est égal à IDCANCEL.

## <a name="configuring-the-connection"></a>Configuration de la connexion

le point d’entrée [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) peut être appelé à partir de [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) ou, sur Windows XP, à partir de [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).

Pour appeler [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) à partir de [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga), définissez l' \_ option RASEO CustomScript dans l’entrée de l’annuaire téléphonique pour la connexion. Consultez le membre **dwfOptions** de [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) pour obtenir une description des options d’entrée de l’annuaire téléphonique. Utilisez les fonctions [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) et [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) pour définir cette option par programmation.

**Windows XP :** Pour appeler [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) à partir de [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala), l’appel à **rasdial** doit spécifier une structure [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) , et cette structure doit spécifier l' \_ indicateur UseCustomScripting RDEOPT. En outre, l’entrée de l’annuaire téléphonique pour la connexion doit spécifier l' \_ option RASEO CustomScript comme décrit dans le paragraphe précédent.

## <a name="invoking-the-custom-scripting-dll"></a>Appel de la DLL de script personnalisé

Si l’utilisateur active une connexion pour une entrée de l’annuaire téléphonique pour laquelle RASEO \_ CustomScript est défini, Ras appelle la dll de script personnalisé. Dans ce scénario, RAS appelle la DLL de script personnalisé à partir de [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga).

Pour appeler la DLL de script personnalisé par programmation, établissez la connexion à l’aide de la fonction [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) . sur Windows XP, la fonction [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) appelle également la DLL de script personnalisé.

 

 