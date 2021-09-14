---
title: Utilisation des marqueurs
description: Utilisation des marqueurs
ms.assetid: b801c985-4ec7-441e-9f8a-40c69b1299a9
keywords:
- Windows Media Format SDK, marqueurs
- ASF (Advanced Systems Format), marqueurs
- ASF (format des systèmes avancés), marqueurs
- ASF (Advanced Systems Format), recherche de marqueurs
- ASF (format de systèmes avancés), recherche de marqueurs
- marqueurs, à propos de
- marqueurs, ajout
- marqueurs, suppression
- marqueurs, récupération
- marqueurs, recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cc585b8c71e3bfbae85953650809ad031d36a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195908"
---
# <a name="using-markers"></a>Utilisation des marqueurs

Un *marqueur* est un point nommé dans un fichier ASF. Chaque marqueur se compose d’un nom et d’une heure associée, mesuré comme un décalage par rapport au début du fichier. Une application peut utiliser des marqueurs pour affecter des noms à différents points dans le contenu, afficher ces noms à l’utilisateur, puis rechercher les positions des marqueurs. Une application peut ajouter ou supprimer des marqueurs d’un fichier ASF existant.

L’interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) contient des méthodes permettant d’utiliser des marqueurs. L’objet éditeur de métadonnées prend en charge l’ajout et la suppression de marqueurs. Les objets Writer et Reader peuvent récupérer des marqueurs, mais ils ne peuvent pas ajouter ou supprimer des marqueurs.

## <a name="adding-markers"></a>Ajouter des marqueurs

Pour ajouter un marqueur, interrogez l’éditeur de métadonnées pour l’interface **IWMHeaderInfo** . Appelez ensuite la méthode [**IWMHeaderInfo :: AddMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) , en spécifiant le nom du marqueur sous la forme d’une chaîne de caractères larges et le temps en unités de 100 nanosecondes. L’heure ne doit pas dépasser la durée du fichier. Deux marqueurs peuvent avoir la même heure.

L’exemple suivant ajoute plusieurs marqueurs à un fichier :


```C++
IWMMetadataEditor *pEdit = 0;
IWMHeaderInfo     *pInfo = 0;

// Create the metadata editor object.

WMCreateEditor(&pEdit);
pEdit->Open(L"C:\\example.wmv");
pEdit->QueryInterface(IID_IWMHeaderInfo, (void**)&pInfo);

// Add the markers. Note that we add the last ones first. Do this when possible
// for improved performance when writing the markers to the file.
hr = pInfo->AddMarker(L"End",  520000000);   // 52 sec.
hr = pInfo->AddMarker(L"Segue",  350000000); // 35 sec.
hr = pInfo->AddMarker(L"Intro",  15000000);  // 1.5 sec.

// Commit changes and clean up.

pEdit->Flush();
pEdit->Close(); 
pInfo->Release();
pEdit->Release();

```



## <a name="removing-markers"></a>Supprimer des marqueurs

Pour supprimer un marqueur, appelez [**IWMHeaderInfo :: RemoveMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker), en spécifiant l’index du marqueur à supprimer. Les marqueurs sont automatiquement triés dans l’ordre chronologique plus important, de sorte que l’index 0 est toujours le premier marqueur. Notez que l’appel de **RemoveMarker** modifie les numéros d’index des marqueurs qui suivent. Le code suivant, où *pinfo* est un pointeur vers une interface **IWMHeaderInfo** , supprime tous les marqueurs d’un fichier :


```C++
WORD count = 0;
pInfo->GetMarkerCount(&count);
while (count--)
{
    pInfo->RemoveMarker(0);
}

```



## <a name="retrieving-markers"></a>Récupération des marqueurs

Pour récupérer le nom et l’heure d’un marqueur, procédez comme suit :

1.  Appelez la méthode [**IWMHeaderInfo :: GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) pour déterminer le nombre de marqueurs que contient le fichier.
2.  Récupérez la taille de la chaîne nécessaire pour contenir le nom du marqueur. Pour ce faire, appelez la méthode [**IWMHeaderInfo :: GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) . Spécifiez l’index du marqueur à récupérer, et **null** pour la mémoire tampon de la chaîne (paramètre *pwszMarkerName* ). La méthode retourne la longueur de la chaîne, y compris le caractère « \\ 0 » de fin, dans le paramètre *pcchMarkerNameLen* .
3.  Allouez une chaîne de caractères larges pour recevoir le nom.
4.  Appelez à nouveau **GetMarker** , mais cette fois, vous transmettez l’adresse de la chaîne dans le paramètre *pwszMarkerName* . La méthode écrit le nom du marqueur dans la chaîne et retourne l’heure du marqueur dans le paramètre *pcnsMarkerTime* .

Le code suivant parcourt chaque marqueur dans l’ordre et récupère le nom et l’heure :


```C++
WORD cMarkers = 0;
HRESULT hr = pInfo->GetMarkerCount(&cMarkers);

WCHAR *wszName = 0;
WORD  len = 0;
for (WORD iMarker = 0; iMarker < cMarkers; ++iMarker)
{
    QWORD rtTime = 0;
    WORD req_len = 0;
    hr = pInfo->GetMarker(iMarker, 0, &req_len, &rtTime);
    
    // Reallocate if necessary.
    if (len < req_len)
    {
        delete[] wszName;
        wszName = new WCHAR[req_len];
        len = req_len;
    }
    hr = pInfo->GetMarker(iMarker, wszName, &req_len, &rtTime);
    // Display the name...
}
delete[] wszName;

```



## <a name="seeking-to-a-marker"></a>Recherche d’un marqueur

Pour démarrer la lecture à partir d’un emplacement de marqueur, appelez la méthode [**IWMReaderAdvanced2 :: StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) de l’objet lecteur, en spécifiant l’index du marqueur. Les paramètres restants sont identiques à ceux de la méthode [**IWMReader :: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) . L’exemple suivant interroge le lecteur pour obtenir l’interface [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) et recherche le premier marqueur.


```C++
IWMReaderAdvanced2 *pReader2 = 0
WORD iMarkerIndex = 0;
hr = pReader->QueryInterface(IID_IWMReaderAdvanced2, (void**)&pReader2);
if (SUCCEEDED(hr))
{
    hr = pPlayer2->StartAtMarker(iMarkerIndex, 0, 1.0, 0);
    pPlayer2->Release();
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker)
</dt> <dt>

[**Utilisation des métadonnées**](working-with-metadata.md)
</dt> </dl>

 

 




