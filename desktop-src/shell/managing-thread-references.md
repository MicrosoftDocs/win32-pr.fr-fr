---
description: Cet article contient des informations sur la gestion des références de thread à l’aide des fonctions des fonctions utilitaires légères de l’interpréteur de commandes.
ms.assetid: d8d479fd-c45a-4dfa-b496-76abc7c09a42
title: Gestion des références de thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b629cd97c99e3b30e66810b5f54720d0dbb1c87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973367"
---
# <a name="managing-thread-references"></a>Gestion des références de thread

Cet article contient des informations sur la gestion des références de thread à l’aide des fonctions des fonctions utilitaires légères de l’interpréteur de commandes.


Des situations se produisent lorsqu’un thread parent doit être maintenu actif pendant la durée de vie d’un thread enfant. Par exemple, si un objet COM (Component Object Model) est créé sur le thread parent et marshalé vers le thread enfant, ce thread parent ne peut pas se terminer avant le thread enfant. Pour ce faire, l’interpréteur de commandes fournit ces fonctions.

-   [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref)
-   [**SHSetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref)
-   [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref)

Utilisez ces fonctions dans votre thread parent comme indiqué ici.

1.  Déclarez une procédure de thread définie par l’application suivant la forme de la fonction [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) .

    ``` syntax
    DWORD WINAPI ThreadProc(LPVOID lpParameter);
    ```

2.  Dans votre [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)), appelez [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref) pour créer une référence au thread. Cela fournit un pointeur vers une instance de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Ce **IUnknown** utilise la valeur pointée par *pcRef* pour conserver un décompte de références. Tant que ce nombre est supérieur à 0, le thread reste actif.
3.  En utilisant ce pointeur vers [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), appelez [**SHSetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref) dans votre [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)). Cela définit la référence afin que les appels suivants à [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref) aient une valeur à récupérer.
4.  Si votre [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) crée un autre thread, le *ThreadProc* de ce thread peut appeler [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref) avec le pointeur vers [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) obtenu par [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref). Cela incrémente le nombre de références vers lequel pointe le paramètre *pcRef* dans **SHCreateThreadRef**.
5.  Créez le thread. Cela s’effectue généralement en appelant [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread), en passant un pointeur à votre [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) dans le paramètre *pfnThreadProc* . Transmettez également l' \_ \_ indicateur de référence de thread CTF dans le paramètre *dwFlags* . Le thread est actif tant que *ThreadProc* est en cours d’exécution.
6.  Quand un thread enfant est créé, transmettez l’indicateur **CTF \_ Ref \_ compté** dans le paramètre *dwFlags* de l’appel à son [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread).
7.  À mesure que les threads enfants sont terminés et libérés, la valeur vers laquelle pointe le *pcRef* du thread parent diminue. Une fois tous les threads enfants terminés, le [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) d’origine peut terminer et libérer la référence de thread finale, en supprimant le décompte de références à 0. À ce stade, la référence au thread d’origine ouvert par [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread) est libérée et le thread est terminé.

Une autre fonction associée est [**SHReleaseThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreleasethreadref). Cette fonction est appelée par [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) si le thread a été créé à l’aide de [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread) avec l’indicateur de **\_ \_ référence de thread CTF** . Toutefois, l’opération *ThreadProc* n’est pas nécessaire pour le faire implicitement. L’appel de [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur le pointeur vers [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) obtenu par le biais de [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref) est tout ce qui doit être effectué.

 

 
