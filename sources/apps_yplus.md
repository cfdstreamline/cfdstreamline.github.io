---
layout: single
classes: wide
toc: false
---

<script src="../../assets/apps/yplus.js" defer> </script>

<form>
  <table style="width:100%">
    <tr>
      <th><label for="Uinf">U<sub>&infin;</sub>								</label></th>
      <th><input type="text" size="20" id="Uinf" name="Uinf" value="1.0">				</th>
      <th>[m/s]																		</th>
      <th>freestream velocity															</th>
    </tr>
    <tr>
      <th><label for="rho">&rho;<sub>&infin;</sub>							</label></th>
      <th><input type="text" size="20" id="rho" name="rho" value="1.225">				</th>
      <th>[kg/m3]																		</th>
      <th>freestream density															</th>
    </tr>
    <tr>
      <th><label for="mu">&mu;<sub>&infin;</sub>								</label></th>
      <th><input type="text" size="20" id="mu" name="mu" value="0.000018375">			</th>
      <th>[kg/m*s]																	</th>
      <th>freestream dynamic viscosity												</th>
    </tr>
    <tr>
      <th><label for="L">L													</label></th>
      <th><input type="text" size="20" id="L" name="L" value="1.0">					</th>
      <th>[m]																			</th>
      <th>reference length															</th>
    </tr>
    <tr>
      <th><label for="yPlus">Target y<sup>+</sup>								</label></th>
      <th><input type="text" size="20" id="yPlus" name="yPlus" value="1.0">			</th>
      <th>[-]																			</th>
      <th>required y<sup>+</sup>														</th>
    </tr>
    <tr>
      <th><label for="Ds">&Delta;s											</label></th>
      <th><input type="text" size="20" id="Ds" name="Ds" value="-">								</th>
      <th>[mm]																			</th>
      <th>first element height														</th>
    </tr>
    <tr>
      <th><label for="Rex">Re													</label></th>
      <th><input type="text" size="20" id="Rex" name="Rex" value="-"> 							</th>
      <th>[-]																			</th>
      <th>Reynolds number																</th>
    </tr>
  </table>
  <button type="button" class="btn btn--primary" onclick="yPlus2Ds(this.form)">Calculate</button>
</form>
